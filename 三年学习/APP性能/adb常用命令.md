# 基础命令

显示系统中全部设备（连接中显示device/断开连接显示offiline）：adb devices  (会自动启动abd服务)

开启或者关闭adb服务（abd时通过adb服务向手机端发送消息）：adb start-server/ adb kill-server  

连接或者断开连接设备： adb connect ip:port/ adb disconnect ip:port

安装卸载软件包：adb install APK路径 参数[-r]覆盖安装时保留数据和缓存文件/adb uninstall apk包名（卸载androd系统中的名字） [-k]卸载时保留数据和缓存文件   

获取所有安装的软件包名：adb shell pm list packages [-s]列出系统应用的所有包名  [-3] 第三方应用市场安装的包名 

显示当前打开的软件包名和当前界面名：  

        windows:adb shell dumpsys window | findstr mCurrentFocus  

        mac/linux:adb shell dimpsys window | grep mCurrentFocus  

eg:包名(package):决定程序的唯一性（非软件名称）  

     界面名(activity):暂时理解为一个界面名，对应着一个界面。  

清理应用数据和缓存：adb shell pm clear (apk包名)  

启动停止应用：adb shell am start 包名/Activity  /adb shell am force-stop apk包名  

上传与下载文件：adb push 电脑路径 手机文件夹路径  / adb pull 手机文件路径 电脑文件路径

# 重要命令

## 获取错误日志信息

打开被测应用程序，进入触发缺陷位置,不触发缺陷->使用查看日志命令:adb logcat >指定文件-> 触发缺陷->获取日志信息->Ctrl+c结束命令  

# 性能测试命令

## 测试启动时间命令：

### 冷启动启动应用：adb shell am start -W 包名/Activity [-S] 启动前都杀死程序  [-R] 表示重复的次数

### 热启动：

* adb shell input keyevent 3
* adb shell am start -W 包名/界面名

### 常见指标：

ThisTime:当前activety的时间

TotalTime：应用的启动时间，包括创建进程，app初始化，activity初始化到界面显示  

WaitTime:前一个activity pause 的时间+TotalTime  

## 获取内存：略

## CPU:略

。。。。。。  

## 稳定性测试命令--Monkey(没啥用)使用appium：通过长时间的无序操作，检查应用程序是否有异常。如闪退，无响应

### 命令：adb shell monkey -p 包名 -v 次数 >日志文件  [-p]指定包 [-v]指定日志详细程度,其中’-v -v -v‘最详细  []







  








