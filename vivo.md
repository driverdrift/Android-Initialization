```
adb install "C:\My Data\Software Repository\Android\AppManager_v4.0.5.apk"
pm uninstall --user 0 com.vivo.secime.service  # 安全键盘
com.vivo.secime.service  # 安全键盘
# 
```
Setup > System manage and upgrade > input: close `safe input` option to generate a hidden config that use common keyboard to input password, otherwise will exit when input password when safekeyboard is uninstalled.
If uninstall this app without generate a hidden config first, you can run the code below to recover it first:
```
# if you run `pm uninstall --user 0 com.vivo.secime.service` before,then the package is still existed.
pm install-existing com.vivo.secime.service  # install for user: 0, or you can run the code below:

cmd package install-existing com.vivo.secime.service # also you can run the code below:

pm list packages -f | grep com.vivo.secime.service  # get the path; note: the path changes every time the app is reinstalled
pm install /data/app/.../base.apk  # no =com.vivo.secime.service
```
