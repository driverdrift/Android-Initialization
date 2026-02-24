# pm list packages -s | wc -l
374
```
pm list packages -s | sort | cut -d':' -f2
```
Packages that support manual uninstallation but are restricted via ADB.  
11 - 1 = 10
```
# com.android.BBKClock # 闹钟时钟；可手动卸载
# com.android.bbkmusic # i 音乐；可手动卸载
# com.bbk.theme # i 主题；可手动删除
# com.iqoo.secure # i 管家；可以手动删除
# com.vivo.agent # Jovi语音；可手动删除
# com.vivo.email # 电子邮件；可手动删除
# com.vivo.gallery # 相册；可手动删除；但不必要删除
# com.vivo.game # 游戏中心；可手动删除
# com.vivo.health # vivo健康；可手动删除
# com.vivo.vtouch # 扫描；可手动卸载
# com.vivo.wallet # 钱包；需要手动删除
```

```
# --user 0 android # Android 系统；删除后系统会重启，重启后会自动重新安装该包
--user 0 android.ext.services # Android Services Library；提供一些可独立更新的系统扩展服务
--user 0 android.overlay.common # android.overlay.common；系统资源覆盖包
--user 0 android.overlay.target # android.overlay.target；系统资源覆盖（RRO）目标包
--user 0 android.overlay.vivoresrro # android.overlay.vivoresrro；vivo 设备厂商提供的系统资源覆盖包
--user 0 android.overlay.vrro # android.overlay.vrro
--user 0 android.qvaoverlay.common # android.qvaoverlay.common；厂商提供的系统资源覆盖包
--user 0 com.amap.android.location # 网络位置
# com.android.BBKClock # 闹钟时钟；可手动卸载
# com.android.BBKCrontab # 定时任务
com.android.VideoPlayer # i 视频
--user 0 com.android.adservices.api # Android 系统；广告服务
--user 0 com.android.backupconfirm # com.android.backupconfirm
com.android.bbk.lockscreen3 # 一键锁屏
com.android.bbkcalculator # 计算器
--user 0 com.android.bbklog # 日志信息采集
# com.android.bbkmusic # i 音乐；可手动卸载
com.android.bbksoundrecorder # 录音机
# com.android.bips # 打印
# --user 0 com.android.bluetooth # 蓝牙
--user 0 com.android.bluetoothmidiservice # Bluetooth MIDI Service；支持通过蓝牙传输 MIDI 数据从而控制乐器
--user 0 com.android.browser # BrowserPlug；AOSP 浏览器组件；在新版本 Android 中已被替代
--user 0 com.android.calllogbackup # Call Log Backup/Restore；通话记录备份/恢复服务。
# --user 0 com.android.camera # 相机
--user 0 com.android.cameraextensions # CameraExtensionsProxy；提供相机扩展功能接口给第三方或系统相机应用从而使用高级功能如夜景模式
--user 0 com.android.captiveportallogin # 登录WLAN网络；处理需要网页验证的 Wi-Fi 网络，弹出登陆页面
# com.android.carrierconfig # com.android.carrierconfig；根据移动运营商提供的配置调整系统行为
--user 0 com.android.carrierconfig.overlay.common # com.android.carrierconfig.overlay.common；覆盖 com.android.carrierconfig 默认资源和配置
--user 0 com.android.carrierdefaultapp # 运营商通知
# com.android.cellbroadcastreceiver # 无线紧急警报
--user 0 com.android.cellbroadcastreceiver.overlay.common # com.android.cellbroadcastreceiver.overlay.common
--user 0 com.android.cellbroadcastservice # Cell Broadcast Service
--user 0 com.android.certinstaller # 证书安装程序
--user 0 com.android.companiondevicemanager # 配套设备管理器
--user 0 com.android.connectivity.resources # 系统网络连接资源
# com.android.contacts # 电话与联系人
--user 0 com.android.credentialmanager # Credential Manager
--user 0 com.android.cts.ctsshim # com.android.cts.ctsshim
--user 0 com.android.cts.priv.ctsshim # com.android.cts.priv.ctsshim
# com.android.devicelockcontroller # DeviceLockController
--user 0 com.android.documentsui # com.android.documentsui
--user 0 com.android.dynsystem # Dynamic System Updates
--user 0 com.android.egg # Android Easter Egg
--user 0 com.android.emergency # 急救信息
--user 0 com.android.ext.adservices.api # Android 系统；扩展广告服务模块
--user 0 com.android.externalstorage # 外部存储设备
--user 0 com.android.federatedcompute.services # com.android.federatedcompute.services
# com.android.filemanager # 文件管理
--user 0 com.android.health.connect.backuprestore # com.android.health.connect.backuprestore
--user 0 com.android.healthconnect.controller # Health Connect
--user 0 com.android.hotspot2.osulogin # OsuLogin
--user 0 com.android.htmlviewer # HTML 查看程序
# com.android.incallui # 电话管理
--user 0 com.android.inputdevices # 输入设备
--user 0 com.android.intentresolver # 分享
--user 0 com.android.internal.display.cutout.emulation.corner # 边角刘海屏
--user 0 com.android.internal.display.cutout.emulation.double # 双刘海屏
--user 0 com.android.internal.display.cutout.emulation.hole # 打孔屏
--user 0 com.android.internal.display.cutout.emulation.tall # 长型刘海屏
--user 0 com.android.internal.display.cutout.emulation.waterfall # 瀑布刘海屏
--user 0 com.android.internal.systemui.navbar.gestural # Gestural Navigation Bar
--user 0 com.android.internal.systemui.navbar.gestural_extra_wide_back # Gestural Navigation Bar
--user 0 com.android.internal.systemui.navbar.gestural_narrow_back # Gestural Navigation Bar
--user 0 com.android.internal.systemui.navbar.gestural_wide_back # Gestural Navigation Bar
--user 0 com.android.internal.systemui.navbar.threebutton # 3 Button Navigation Bar
--user 0 com.android.internal.systemui.navbar.transparent # Transparent navigation bar
--user 0 com.android.keychain # 密钥链
--user 0 com.android.localtransport # com.android.localtransport
# com.android.location.fused # 一体化位置信息
--user 0 com.android.managedprovisioning # 工作设置
# com.android.mms # 信息
# com.android.mms.service # 信息
--user 0 com.android.modulemetadata # Module Metadata
--user 0 com.android.mtp # MTP 主机
# --user 0 com.android.networkstack # 网络管理器；删除后会导致黑屏关机，无法开机；但是有时候重启后又可以正常开机，此时包变成 com.android.networkstack.tethering.inprocess，并且无法连接 wifi 或者数据流量。误删后需运行 pm uninstall --user 0 com.android.networkstack.tethering.inprocess && pm install-existing com.android.networkstack && reboot
--user 0 com.android.networkstack.tethering.inprocess # Tethering
com.android.notes # 原子笔记
--user 0 com.android.ondevicepersonalization.services # com.android.ondevicepersonalization.services.OnDevicePersonalizationApplication
--user 0 com.android.ons # com.android.ons
# com.android.packageinstaller # 软件包安装程序
--user 0 com.android.pacprocessor # PacProcessor
# com.android.permissioncontroller # 权限控制器
# com.android.phone # 电话
--user 0 com.android.phone.overlay.common # com.android.phone.overlay.common
# com.android.printspooler # 打印处理服务
--user 0 com.android.providers.blockednumber # 存储已屏蔽的号码
# com.android.providers.calendar # 日历存储
# com.android.providers.contacts # 联系人存储
# com.android.providers.downloads # 内容下载管理器
# com.android.providers.downloads.ui # 下载管理
--user 0 com.android.providers.media # com.android.providers.media
--user 0 com.android.providers.media.module # 媒体
# com.android.providers.settings # 设置存储
# com.android.providers.telephony # 电话和短信存储
--user 0 com.android.providers.userdictionary # 用户字典
--user 0 com.android.proxyhandler # ProxyHandler
--user 0 com.android.rkpdapp # RemoteProvisioner
--user 0 com.android.role.notes.enabled # Notes Role enabled
--user 0 com.android.safetycenter.resources # 安全中心资源
--user 0 com.android.sdksandbox # com.android.sdksandbox
--user 0 com.android.se # SecureElementApplication
# com.android.server.telecom # 通话管理
--user 0 com.android.server.telecom.overlay.common # com.android.server.telecom.overlay.common
# com.android.settings # 设置
--user 0 com.android.settings.overlay.common # com.android.settings.overlay.common
--user 0 com.android.sharedstoragebackup # com.android.sharedstoragebackup
# --user 0 com.android.shell # Shell；删除后无法在 adb 执行 pm uninstall 和 pm install 命令，那如果手动卸载后，装入一个带 su 命令的 shell 会怎样？
--user 0 com.android.simappdialog # Sim App Dialog
--user 0 com.android.smspush # com.android.smspush
--user 0 com.android.soundpicker # 声音
--user 0 com.android.statementservice # Intent Filter Verification Service
com.android.stk # SIM卡应用
--user 0 com.android.storagemanager # 存储空间管理器
# com.android.systemui # 系统界面
--user 0 com.android.systemui.overlay.common # com.android.systemui.overlay.common
--user 0 com.android.systemui.plugin.globalactions.wallet # com.android.systemui.plugin.globalactions.wallet
--user 0 com.android.theme.font.notoserifsource # Noto Serif / Source Sans Pro
--user 0 com.android.traceur # 系统跟踪
--user 0 com.android.uwb.resources # System UWB Resources
--user 0 com.android.vending # Google Play Services Updater
--user 0 com.android.vendors.bridge.softsim # com.android.vendors.bridge.softsim
--user 0 com.android.virtualmachine.res # com.android.virtualmachine.res
--user 0 com.android.vivo.tws.vivotws # vivo TWS
--user 0 com.android.vpndialogs # VpnDialogs
--user 0 com.android.wallpaperbackup # com.android.wallpaperbackup
--user 0 com.android.wallpapercropper # com.android.wallpapercropper
--user 0 com.android.wifi.dialog # com.android.wifi.dialog
--user 0 com.android.wifi.resources # 系统 WLAN 资源
--user 0 com.android.wifi.resources.overlay.common # com.android.wifi.resources.overlay.common
--user 0 com.android.wifi.resources.overlay.target # com.android.wifi.resources.overlay.target
--user 0 com.baidu.input_vivo # 百度输入法定制版
--user 0 com.baidu.map.location # 网络位置
# com.bbk.SuperPowerSave # 超级省电
# com.bbk.account # vivo账号
# com.bbk.appstore # 应用商店
com.bbk.calendar # 日历
# com.bbk.cloud # 云服务
--user 0 com.bbk.facewake # 智能保持亮屏
com.bbk.iqoo.feedback # 意见反馈
--user 0 com.bbk.iqoo.logsystem # 用户体验改进计划服务
# com.bbk.launcher2 # 系统桌面
# com.bbk.lite.theme # 系统美化
--user 0 com.bbk.photoframewidget # 相框
--user 0 com.bbk.scene.databaseprovider # SceneDatabaseProvider
--user 0 com.bbk.scene.launcher.theme # SceneThemeLauncher
# com.bbk.theme # i 主题；可手动删除
--user 0 com.bbk.theme.resources # vivoWallpaperRes
# com.bbk.updater # 系统升级
--user 0 com.fido.client # FIDO认证器
--user 0 com.focal.touch.datashow # DataShow
--user 0 com.focal.touch.sensorcheck # FocalTech Sensor Check
com.funtouch.uiengine # LockScreenStyleEngine
--user 0 com.google.android.accessibility.switchaccess # 开关控制
--user 0 com.google.android.configupdater # ConfigUpdater
--user 0 com.google.android.ext.shared # Android Shared Library
# com.google.android.gms # Google Play 服务
# com.google.android.gsf # Google 服务框架
--user 0 com.google.android.marvin.talkback # Android 无障碍套件
--user 0 com.google.android.onetimeinitializer # Google One Time Init
--user 0 com.google.android.overlay.gmsconfig.common # com.google.android.overlay.gmsconfig.common
--user 0 com.google.android.printservice.recommendation # Print Service Recommendation Service
--user 0 com.google.android.syncadapters.calendar # Google 日历同步
--user 0 com.google.android.webview # Android System WebView
--user 0 com.google.android.wifi.resources.overlay.common # com.google.android.wifi.resources.overlay.common
--user 0 com.google.ar.core # ARCore
# com.iqoo.powersaving # 电池
# com.iqoo.secure # i 管家；可以手动删除
com.mobile.cos.iroaming # iRoamingService
com.mobile.iroaming # 流量商店
--user 0 com.mobiletools.systemhelper # SystemHelper
--user 0 com.nt36xxxtouchscreen.deltadiff # Noise Test
--user 0 com.nttouchscreen.getdata # RawDelta Test
--user 0 com.nvt.touch.sensorcheck # NVT MP Test
--user 0 com.qti.confuridialer # Conference URI Dialer
--user 0 com.qti.diagservices # com.qti.diagservices
# com.qti.dpmserviceapp # com.qti.dpmserviceapp
--user 0 com.qti.ltebc # LTE Broadcast Manager
--user 0 com.qti.qcc # QCC
--user 0 com.qti.qualcomm.datastatusnotification # com.qti.qualcomm.datastatusnotification
--user 0 com.qti.service.colorservice # com.qti.service.colorservice
--user 0 com.qualcomm.atfwd # com.qualcomm.atfwd
--user 0 com.qualcomm.atfwd2 # com.qualcomm.atfwd2
--user 0 com.qualcomm.location # LocationServices
--user 0 com.qualcomm.qcrilmsgtunnel # com.qualcomm.qcrilmsgtunnel
# com.qualcomm.qti.cne # CneApp
--user 0 com.qualcomm.qti.devicestatisticsservice # com.qualcomm.qti.devicestatisticsservice
--user 0 com.qualcomm.qti.dynamicddsservice # com.qualcomm.qti.dynamicddsservice
--user 0 com.qualcomm.qti.modemmbnmode # MBN 测试
--user 0 com.qualcomm.qti.poweroffalarm # 关机闹钟
--user 0 com.qualcomm.qti.qcolor # QColor
--user 0 com.qualcomm.qti.qms.service.trustzoneaccess # com.qualcomm.qti.qms.service.trustzoneaccess
--user 0 com.qualcomm.qti.remoteSimlockAuth # com.qualcomm.qti.remoteSimlockAuth
--user 0 com.qualcomm.qti.ridemodeaudio # RideMode Recording list
--user 0 com.qualcomm.qti.server.qtiwifi # QtiWifiService
--user 0 com.qualcomm.qti.server.wigig.tethering.rro # com.qualcomm.qti.server.wigig.tethering.rro
--user 0 com.qualcomm.qti.simcontacts # SIM卡联系人
# com.qualcomm.qti.telephonyservice # com.qualcomm.qti.telephonyservice
--user 0 com.qualcomm.qti.uim # com.qualcomm.qti.uim
--user 0 com.qualcomm.qti.uimGbaApp # com.qualcomm.qti.uimGbaApp
--user 0 com.qualcomm.qti.workloadclassifier # com.qualcomm.qti.workloadclassifier
--user 0 com.qualcomm.qti.xrcb # XRCB
--user 0 com.qualcomm.qti.xrvd.service # XRVD
--user 0 com.qualcomm.timeservice # com.qualcomm.timeservice
--user 0 com.qualcomm.uimremoteclient # com.qualcomm.uimremoteclient
--user 0 com.qualcomm.uimremoteserver # com.qualcomm.uimremoteserver
--user 0 com.qualcomm.wfd.service # Wfd Service
--user 0 com.quicinc.voice.activation # Qualcomm Voice Assist
# com.ringclip # 铃声剪辑
--user 0 com.rongcard.eid # Eid-Service；金邦达开发的的网络数字身份卡
--user 0 com.sohu.inputmethod.sogou.vivo # 搜狗输入法定制版
--user 0 com.tencent.soter.soterserver # aidlserverdemo；腾讯相关应用的指纹支付和登录功能
# com.vivo.SmartKey # 快捷启动
com.vivo.Tips # 使用技巧
# com.vivo.abe # 智慧引擎
# com.vivo.accessibility # 无障碍
# com.vivo.accessibilityenhance # Accessibility Enhance
# com.vivo.agent # Jovi语音；可手动删除
--user 0 com.vivo.ai.base.copilot # 蓝心小V
com.vivo.ai.copilot # 蓝心小V
--user 0 com.vivo.ai.gptagent # 智慧体
--user 0 com.vivo.aiengine # AI服务引擎
--user 0 com.vivo.aiservice # AIService
com.vivo.alldocuments # vivo万能查看器
--user 0 com.vivo.alphacamera # AlphaCamera
--user 0 com.vivo.android.connectivity.common.resources.overlay # com.vivo.android.connectivity.common.resources.overlay
--user 0 com.vivo.android.connectivity.mainline.common.resources.overlay # com.vivo.android.connectivity.common.resources.overlay
--user 0 com.vivo.android.connectivity.mainline.manufacturer.resources.overlay # com.vivo.android.connectivity.mainline.common.resources.overlay
--user 0 com.vivo.android.connectivity.manufacturer.resources.overlay # com.vivo.android.connectivity.manufacturer.resources.overlay
--user 0 com.vivo.android.wifi.common.resources.overlay # com.vivo.android.wifi.common.resources.overlay
--user 0 com.vivo.android.wifi.mainline.common.resources.overlay # com.vivo.android.wifi.mainline.common.resources.overlay
--user 0 com.vivo.android.wifi.mainline.manufacturer.resources.overlay # com.vivo.android.wifi.mainline.manufacturer.resources.overlay
--user 0 com.vivo.android.wifi.manufacturer.resources.overlay # com.vivo.android.wifi.manufacturer.resources.overlay
# com.vivo.appfilter # 防拉起服务
com.vivo.are # 精彩推荐
# com.vivo.assistant # 重要通知
# com.vivo.audiofx # 音效设置
# com.vivo.base.agent # Jovi语音
# com.vivo.base.gallery # 图像查看
--user 0 com.vivo.base.player # 音频播放器(系统)
# com.vivo.base.vtouch # 扫描
--user 0 com.vivo.basemanager # 手机存储
--user 0 com.vivo.browser # 浏览器
# com.vivo.car.networking # 智能车载
# com.vivo.card # 超级卡包
# com.vivo.carlauncher # 车载launcher
com.vivo.childrenmode # 儿童模式
# com.vivo.cipherchain # 密码保险箱
com.vivo.compass # 指南针
# com.vivo.connbase # 多设备互联
--user 0 com.vivo.connbase.connectcenter # 多设备互联
--user 0 com.vivo.connbase.deviceaccessory # vivo快联
--user 0 com.vivo.connbase.sysui # ControlCenter
# com.vivo.cota # COTA
com.vivo.countdownwidget # 计时器组件
# com.vivo.daemonService # vivo服务
--user 0 com.vivo.defaultPlayer # 视频播放器
com.vivo.deformer # 原景视窗
com.vivo.desktopstickers # 贴纸
com.vivo.devicepower # 设备电量
# com.vivo.devicereg # 设备管理
# com.vivo.doubleinstance # 应用分身
com.vivo.doubletimezoneclock # 时钟天气
--user 0 com.vivo.dr # vivo位置引擎
com.vivo.dream.clock # 时钟（轻简约）
com.vivo.dream.weather # 天气（轻简约）
com.vivo.easyshare # 互传
# com.vivo.email # 电子邮件；可手动删除
--user 0 com.vivo.epm # EPM；能量电源管理
# com.vivo.faceui # FaceUI
# com.vivo.faceunlock # 面部识别
# com.vivo.familycare.local # 健康使用设备
# com.vivo.favorite # 收藏
--user 0 com.vivo.fileobserver # 新增文件
# com.vivo.findphone # 查找
# com.vivo.fingerprint # 指纹与密码
--user 0 com.vivo.fingerprintui # 指纹UI
--user 0 com.vivo.fingerprintvit # 指纹Vit
# com.vivo.floatingball # 悬浮球
--user 0 com.vivo.fuelsummary # 电源信息
--user 0 com.vivo.fuzzylocationmanager # 模糊定位
# com.vivo.gallery # 相册；可手动删除；但不必要删除
# com.vivo.game # 游戏中心；可手动删除
# com.vivo.gamecube # 游戏魔盒
--user 0 com.vivo.gamespace # vivo游戏空间
com.vivo.gametrain # 听音辨位训练场
# com.vivo.gamewatch # GameWatch
# com.vivo.globalanimation # 全局动效
--user 0 com.vivo.globaldragdrop # 超级拖放
# com.vivo.globalsearch # 全局搜索
# com.vivo.health # vivo健康；可手动删除
--user 0 com.vivo.healthservice # 健康服务
com.vivo.healthwidget # 健康组件
# com.vivo.hiboard # 智慧桌面
--user 0 com.vivo.hover # 语音突显悬浮按钮
# com.vivo.hybrid # 快应用框架服务
--user 0 com.vivo.iotserver # IoT服务引擎
com.vivo.launchercopilot # 蓝心小V组件
com.vivo.livewallpaper.parallelworld # 平行世界
# com.vivo.magazine # 阅图锁屏
# com.vivo.minscreen # 小屏
com.vivo.moodcube # 变形器
--user 0 com.vivo.motionrecognition # 智能体感
--user 0 com.vivo.multinlp # VivoLocationServices
# com.vivo.musicwidgetmix # 原子随身听
--user 0 com.vivo.networkimprove # NetworkImprove
--user 0 com.vivo.networkstate # NetworkState
--user 0 com.vivo.nps # vivo体验评价
# com.vivo.numbermark # 陌电识别
# com.vivo.pay # 多场景安全支付服务
# com.vivo.pcsuite # vivo办公套件
# com.vivo.pem # 电量守护
# com.vivo.permissionmanager # 权限管理
--user 0 com.vivo.phonehandoff # 通话接力
--user 0 com.vivo.pie # 功耗体验优化
--user 0 com.vivo.privacylauncher # 隐私桌面
com.vivo.puresearch # 桌面搜索
# com.vivo.pushservice # 推送引擎
# com.vivo.quickpay # 快捷支付
com.vivo.remoteassistant # 远程协助
# com.vivo.safecenter # 安全中心
--user 0 com.vivo.screenagent # 小V帮记
# com.vivo.sdkplugin # vivo服务安全插件
--user 0 com.vivo.secime.service # 安全键盘
# com.vivo.setupwizard # 开机引导
--user 0 com.vivo.share # vivo互传
--user 0 com.vivo.sim.contacts # SIM卡联系人服务
--user 0 com.vivo.simpleiconthemeres # SimpleIconThemeRes
--user 0 com.vivo.singularity # vivo system webview；vivo 定制 System WebView
--user 0 com.vivo.smartLife # 智慧生活服务
--user 0 com.vivo.smartanswer # 电话秘书
# com.vivo.smartmultiwindow # 多任务
com.vivo.smartoffice # vivo文档
# --user 0 com.vivo.smartshot # 超级截屏；删除后失去任何截屏功能
--user 0 com.vivo.smartunlock # 智能解锁
# com.vivo.sos # 紧急呼叫
com.vivo.space # vivo 官网
# com.vivo.sps # SuperProcessSystem
# --user 0 com.vivo.systemuiplugin # 系统界面组件；删除会导致手机黑屏
--user 0 com.vivo.telephonyapp # 移动网络服务
com.vivo.timerwidget # 闹钟组件
# com.vivo.upnpserver # 投屏
# com.vivo.upslide # 交互池
--user 0 com.vivo.vdfs # 跨设备使用(mdfs)
--user 0 com.vivo.vhomeguide # VHome
--user 0 com.vivo.vibrator4d # vibrator4d # 4D 振动服务应用，线性马达效果
--user 0 com.vivo.video.floating # 视频通话美颜
# com.vivo.videoeditor # 视频编辑
--user 0 ccom.vivo.visionaid.builtin # 视觉辅助
--user 0 com.vivo.vivo3rdalgoservice # ImageAlgoService
com.vivo.vivokaraoke # 移动KTV
--user 0 com.vivo.vmdri # 连接中心
# com.vivo.vms # vivo移动服务
--user 0 com.vivo.voicerecognition # 声音识别
# com.vivo.voicewakeup # 语音唤醒
# com.vivo.vtouch # 扫描；可手动卸载
# com.vivo.wallet # 钱包；需要手动删除
com.vivo.weather # 天气
# com.vivo.weather.provider # 天气存储
com.vivo.widget.calendar # 日历组件
com.vivo.widget.cleanspeed # 清理加速组件
com.vivo.widget.gallery # 相册精选
com.vivo.widget.healthcare # 健康关怀
com.vivo.widget.timemanager # 屏幕使用时间组件
com.vivo.widgetweather # 天气组件
# com.vivo.xspace # 原子隐私系统
--user 0 com.vlife.vivo.wallpaper # 动态锁屏服务
--user 0 com.vos.as.vit # 售后服务
--user 0 com.vos.user.vit # 工程菜单
--user 0 com.wapi.wapicertmanage # WAPI 证书管理
# org.codeaurora.ims # org.codeaurora.ims
--user 0 org.ifaa.aidl.manager # aidlserverdemo；统一 Android 生物认证接口标准如指纹支付
--user 0 vendor.qti.hardware.cacert.server # CACertApp；提供系统或硬件层的证书验证
--user 0 vendor.qti.iwlan # vendor.qti.iwlan # 负责 Wi-Fi 通话和运营商 Wi-Fi 数据支持
--user 0 vendor.qti.qesdk.sysservice # QesdkSysApp；为 Qualcomm 芯片上的系统或应用提供 底层硬件接口和扩展功能支持如音频增强，底层诊断与分析
```
