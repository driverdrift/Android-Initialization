```
adb shell pm uninstall --user 0 com.vivo.browser # 浏览器
adb shell pm uninstall --user 0 com.sohu.inputmethod.sogou.vivo # 搜狗输入法定制版
adb shell pm uninstall --user 0 com.baidu.input_vivo # 百度输入法定制版
```
# Configure keyboard
```
$apks = Get-ChildItem "C:\My Data\Software Repository\Android\com.google.android.inputmethod.latin.*.apk"
adb install-multiple $apks.FullName  # Gboard
```
Enable Gboard and set as default keyboard.  
⚠️ Then `Setup > System manage and upgrade > input`: close `safe input` option to generate a hidden config that use common keyboard to input password, otherwise will exit when input password when safekeyboard is uninstalled.
If uninstall this app without generate a hidden config first, you can run the code below to recover it first:  
if you run `pm uninstall --user 0 com.vivo.secime.service  # 安全键盘` before,then the package is still existed.
```
pm install-existing com.vivo.secime.service  # install for user: 0, or you can run the code below:

cmd package install-existing com.vivo.secime.service # also you can run the code below:

pm list packages -f | grep com.vivo.secime.service  # get the path; note: the path changes every time the app is reinstalled
pm install /data/app/.../base.apk  # no =com.vivo.secime.service
# if you run `pm uninstall com.vivo.secime.service` before,then the package is still existed, but the file path will be fixed as below sometimes:
pm install /system/app/SecIME/SecIME.apk  # no =com.vivo.secime.service
```
```
# adb install "C:\My Data\Software Repository\Android\AppManager_v4.0.5.apk"  # debug
```
# third-party app
```
for pkg in $(pm list packages -3 | cut -d':' -f2 | grep -Ev '^(io\.github\.muntashirakon\.AppManager|com\.google\.android\.inputmethod\.latin)'); do
	echo "Trying to unistall: $pkg"
	pm uninstall "$pkg"
done
```

# system app（会导致收不到短信和热点，因此白名单法不可靠）
```
# white list
WHITELIST=(
	android
	com.android.bluetooth
	com.android.camera
	com.android.networkstack
	com.android.shell
	com.vivo.smartshot
	com.vivo.systemuiplugin
	com.android.providers.media.module
	com.google.android.webview
)

is_whitelisted() {
	for w in "${WHITELIST[@]}"; do
		[ "$w" = "$1" ] && return 0
	done
	return 1
}

pm list packages -s | cut -d':' -f2 | while read pkg; do
	if is_whitelisted "$pkg"; then
		echo "Skip (whitelisted): $pkg"
	continue
	fi

	echo "Trying to uninstall: $pkg"
	pm uninstall "$pkg" || pm uninstall --user 0 "$pkg"
done
```
