# 手机上获取 APK（无需自己安装 Android Studio）

本项目附带 GitHub Actions 云端构建流程。它会在 GitHub 的云端机器上编译 APK，并把 APK 作为构建产物提供下载。**这不是已经编译好的 APK**；需要先把项目上传到 GitHub。

## 操作步骤
1. 用浏览器打开 https://github.com/ 并登录或注册账号。
2. 创建一个新的 Repository（仓库），名称可填 `cow-offwork-app`，选择 Public 或 Private 均可。
3. 在仓库页面选择 Add file → Upload files，把解压后的项目文件和文件夹全部上传到仓库根目录，然后 Commit changes。注意 `.github/workflows/build-apk.yml` 也必须上传。
4. 打开仓库上方的 Actions 标签页，选择 `Build Android APK`，点击 Run workflow → Run workflow。
5. 等待任务完成（绿色勾号）。打开这次运行记录，在页面底部 Artifacts 区域下载 `cow-offwork-debug-apk`。
6. 解压下载的 ZIP，找到 `app-debug.apk`，点击安装。若系统提示，允许浏览器或文件管理器“安装未知应用”。

## 重要说明
- 首次安装可能需要允许“安装未知应用”。
- 这是 debug 测试包，适合个人试用；正式发布前还需要生成并妥善保管正式签名密钥。
- 项目离线运行，不需要把网页托管到网上；设置与宠物数据保存在 APP 本地。
- 如果 GitHub Actions 报错，把错误页面截图发给我，我可以继续修复。
