List of devices attached
```
adb devices
```
Run remote shell commands on a device.
```
adb shell
adb -s <target-device-ID> shell  # If more than one device/emulator
```

List packages in shell.
```
pm list packages				# List all installed packages
pm list packages -s				# List only system packages
pm list packages -3				# List only third-party (user-installed) packages
pm list packages -3 | wc -l		# wc (word count), -l (Lines)
pm list packages -f				# List packages with their associated file paths.
pm list packages | grep xxx		# Search xxx
```

```
pm list packages -e							# Lists only applications that are currently enabled.
pm list packages -d							# Lists only applications that are currently disabled.
pm disable-user --user 0 com.miui.weather2	# for current user
pm disable com.miui.weather2				# some app need root
pm enable com.miui.weather2					# set new state: enabled
pm hide --user 0 com.miui.weather2			# need root
```

Prints the current state of all activities and activity stacks in the system.
```
dumpsys activity activities
dumpsys activity services | grep xxx
```

```
adb install path/to/app.apk
adb install -r path/to/app.apk  # keep data
adb install -r -d  path/to/app.apk # keep data, allow downgrade

adb uninstall <name of package>  # some app need root
pm uninstall --user 0 <name of package>
pm uninstall -k --user 0 com.miui.weather2	# -k (Keep Data and Cache Directories)
```

# User
```
pm list users  # List all users on the device.
pm list packages --user 0
pm create-user <USER_NAME>  # will return an user id
pm remove-user <user_id>  # should log out the target user first
```

# Uninstall
Otherwise uninstall such as com.android.provision will cause system panic.
```
for pkg in $(pm list packages | cut -d':' -f2 | grep -Ev '^(com\.android|com\.google|com\.qti)'); do
	echo "Trying to unistall: $pkg"
	pm uninstall --user 0 "$pkg"
done
```

all path in package:/data/app/
```
for pkg in $(pm list packages -3 | cut -d':' -f2); do
	echo "Trying to unistall: $pkg"
	pm uninstall --user 0 "$pkg"
done
```

debug
```
pm path package-name
adb pull /data/app/xxx/base.apk
dumpsys package com.xiaomi.gamecenter
aapt dump badging MiGameCenter.apk | grep application-label  # aapt（in Android SDK)
```
# Export
For an app with many apks.
```
pm list packages -f | grep com.google.android.inputmethod.latin  # only show one path.
pm path com.google.android.inputmethod.latin  # show all paths
```
```
adb shell pm path com.google.android.inputmethod.latin |
ForEach-Object {
    $path = ($_ -split ":")[1].Trim()
    $name = Split-Path $path -Leaf
    adb pull $path "com.google.android.inputmethod.latin.$name"
}
```

# Wireless debugging
First use an usb,then set adbd process of target device in TCP mode
```
adb tcpip 5555  # Set target device to listen for a TCP/IP connection on port 5555.
# Temporary listener; will revert after device reboot.
adb shell "netstat -an | grep 5555"  # result is:
tcp6       0      0 [::]:5555               [::]:*                  LISTEN
```
You can also enable wireless debug directly without usb connect first.  
Enable wireless debug in develop mode.
```
adb pair 192.168.0.110:pair_port  # Enter pairing code
adb connect 192.168.0.110:connect_port
```


Connect device via internet.
```
adb connect 192.168.0.110:5555
netstat -an | grep 5555  # result is:
tcp6       0      0 [::]:5555               [::]:*                  LISTEN
tcp6       0      0 ::ffff:192.168.0.1:5555 ::ffff:192.168.0.:58047 ESTABLISHED
```
Recover device to usb mode.
```
adb usb  # Set target device to restart in USB mode, also you can run as code below
adb reboot  # adbd reverts to USB mode by default.
netstat -an | grep 5555  # result is (This TIME_WAIT record will disappear in a few seconds.):
tcp6       0      0 ::ffff:192.168.0.1:5555 ::ffff:192.168.0.:58047 TIME_WAIT
```

Remove connected device
```
adb devices
adb disconnect 192.168.0.110:5555  # to remove remote connect, you can also run as code below:
adb kill-server; adb start-server
```
