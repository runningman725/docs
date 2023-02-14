1.安装jdk
2.安装android studio
3.安装flutter sdk
https://docs.flutter.dev/development/tools/sdk/releases
配置path
然后cmd 检查flutter --version，查看有没有版本号
4.配置flutter 国内镜像
https://docs.flutter.dev/community/china

这两项添加到环境变量
PUB_HOSTED_URL=https://pub.flutter-io.cn
FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
添加完了之后，cmd 打开 flutter doctor检查

flutter devices //flutter可运行设备
flutter run //默认运行
flutter run -d all//运行所有平台
flutter run -d windows//运行windows平台



