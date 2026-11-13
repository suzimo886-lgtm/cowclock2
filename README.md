# 牛马下班倒计时 Android APP（手机体验版）

原生 Android WebView 外壳，安装后桌面显示“牛马下班倒计时”图标，点击直接进入 APP，不需要打开 Chrome。首页使用手机优先布局，包含下班倒计时、实时收入估算、宠物互动、休息计时、今日目标和收入记录；页面离线运行。

## 云端构建 APK
本项目已附 GitHub Actions 工作流：`.github/workflows/build-apk.yml`。用手机也可以按 `手机上获取APK.md` 的步骤上传到 GitHub 并触发云端构建，然后从 Actions 的 Artifacts 下载 `app-debug.apk`。

## 本地构建
Android Studio 打开项目，使用 JDK 17、Gradle 8.9、Android SDK Platform 35，执行 `gradle assembleDebug`。APK 输出在 `app/build/outputs/apk/debug/app-debug.apk`。

## 说明
- 当前交付是可云端构建的 Android 项目，不是已经编译好的 APK。
- Debug APK 供测试安装；正式发布需要配置正式签名。
- 收入为按设置时薪和工作时间估算，不代表实际发薪金额。
