List of devices attached
```
adb devices
```

```
adb shell
```

```
pm list packages
```

List third-party packages
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
pm disable com.miui.weather2				# need root
pm enable com.miui.weather2					# set new state: enabled
```

```
pm uninstall --user 0 <name of package>
pm uninstall -k --user 0 com.miui.weather2	# -k (Keep Data and Cache Directories)
```

Otherwise unistall such as com.android.provision will cause system panic.
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

# Wireless debugging
```
adb tcpip 5555  # Set target device to listen for a TCP/IP connection on port 5555.
# Temporary listener; will revert after device reboot.
adb shell netstat -an | grep 5555  # result is:
tcp6       0      0 [::]:5555               [::]:*                  LISTEN

```

```
adb connect 192.168.0.110:5555
netstat -an | grep 5555  # result is:
tcp6       0      0 [::]:5555               [::]:*                  LISTEN
tcp6       0      0 ::ffff:192.168.0.1:5555 ::ffff:192.168.0.:58047 ESTABLISHED
```

```
adb usb  # Set target device to restart in USB mode,also you can run as code below
adb reboot  # adbd reverts to USB mode by default.
netstat -an | grep 5555  # result is (This TIME_WAIT record will disappear in a few seconds.):
tcp6       0      0 ::ffff:192.168.0.1:5555 ::ffff:192.168.0.:58047 TIME_WAIT
```
