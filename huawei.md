# Configure keyboard
```
adb install "C:\My Data\Software Repository\Android\_com.google.android.inputmethod.latin_10.4.04.361808908-lite_release-arm64-v8a-52619238_minAPI27(arm64-v8a)(nodpi)_apkmirror.com.apk"

adb install "C:\My Data\Software Repository\Android\com.android.chrome_83.0.4103.106-410410673_minAPI24(arm64-v8a,armeabi-v7a)(nodpi)_apkmirror.com.apk"
```
Enable Gboard and set as default keyboard.
close safe input option
# third-party app
```
for pkg in $(pm list packages -3 | cut -d':' -f2 | grep -Ev '^(io\.github\.muntashirakon\.AppManager|com\.google\.android\.inputmethod\.latin)'); do
	echo "Trying to unistall: $pkg"
	pm uninstall "$pkg"
done
```
# system app
先关闭 智慧多窗再卸载，不然会有配置图标。
其他设置也是
```
pm uninstall com.huawei.ohos.suggestion # 小艺建议
pm uninstall com.huawei.health # 运动健康
pm uninstall --user 0 com.huawei.himovie # 华为视频
pm uninstall --user 0 com.huawei.music # 音乐
pm uninstall com.huawei.hwireader # 阅读
pm uninstall --user 0 com.huawei.android.thememanager # 主题
pm uninstall --user 0 com.huawei.wallet # 华为钱包
pm uninstall com.vmall.client # 华为商城
# pm uninstall --user 0 com.huawei.appmarket # 华为应用市场
pm uninstall com.huawei.meetime # 畅连
pm uninstall com.huawei.gamebox # 游戏中心
pm uninstall com.huawei.educenter # 华为教育中心
pm uninstall com.huawei.notepad # 备忘录
pm uninstall com.huawei.ohos.smarthome # 智慧生活 ？？？
pm uninstall --user 0 com.huawei.ohos.smarthome # 智慧生活 ？？？ 可以通过手动卸载
pm uninstall com.huawei.android.findmyphone # 查找设备
pm uninstall com.huawei.mirror # 镜子
pm uninstall com.hicloud.android.clone # 手机克隆
pm uninstall com.huawei.compass # 指南针
pm uninstall --user 0 com.android.stk # SIM 卡应用 # 图标还在，过一会自动没了
pm uninstall com.android.storagemanager # 手机管家 # 图标还在
pm uninstall --user 0 com.huawei.phoneservice # 我的华为
pm uninstall com.huawei.hiskytone # 天际通
pm uninstall com.huawei.lives # 生活服务
pm uninstall com.huawei.mycenter # 会员中心
pm uninstall com.huawei.videoeditor # 花瓣剪辑
pm uninstall com.huawei.email # 电子邮件
pm uninstall com.huawei.android.tips # 玩机技巧
pm uninstall --user 0 com.huawei.hidisk # 云空间
pm uninstall com.huawei.hifolder # 精品推荐
pm uninstall com.petal.litegames # 花瓣轻游
pm uninstall com.huawei.ohos.inputmethod # 小艺输入法
pm uninstall com.huawei.android.totemweather # 天气
pm uninstall com.huawei.calculator # 计算器
pm uninstall com.huawei.soundrecorder # 录音机
pm uninstall --user 0 com.android.providers.calendar # 日历 # 卸载了图标还在
pm disable-user com.android.providers.calendar # 日历 # 卸载了图标还在
pm uninstall --user 0 com.android.providers.contacts # 联系人
pm uninstall --user 0 com.huawei.intelligent # 智慧助手
pm uninstall --user 0 com.huawei.browser # 浏览器
pm disable-user com.huawei.android.hwouc # 软件更新
pm uninstall --user 0 com.huawei.magazine # 杂志锁屏
pm uninstall --user 0 com.huawei.aod # 熄屏显示
pm uninstall --user 0 com.huawei.livewallpaper.paradise # 超级壁纸
pm uninstall --user 0 com.huawei.vassistant # 智慧语音
pm uninstall --user 0 com.huawei.ohos.search # 全局搜索数据服务
pm uninstall --user 0 com.huawei.search # 智慧搜索
pm uninstall com.huawei.browser.fa # 浏览器
pm uninstall --user 0 com.huawei.wallet.facard # 钱包
pm uninstall com.huawei.ohos.health # 运动健康
pm uninstall --user 0 com.huawei.gameassistant # 应用助手
pm uninstall --user 0 com.baidu.input_huawei # 百度输入法华为版
pm uninstall --user 0 com.huawei.fastapp # 快应用中心
pm uninstall --user 0 com.huawei.hwdockbar # 智慧多窗
```
