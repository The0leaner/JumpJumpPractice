# PlayJumpJumpWithMouse
微信小游戏 跳一跳(due to 2017.12.27)

## 契机
微信主推叫跳一跳的小程序小游戏，手残认证，但还是发现了办法提高好友的好友排名。
* thanks to @easyworld @RoyZ

## 原理
用usb调试安卓手机，用adb截图并用鼠标测量距离，然后计算按压时间后模拟按压。
```
adb shell input swipe <x1> <y1> <x2> <y2> [duration(ms)] (Default: touchscreen) # 模拟长按
adb shell screencap <filename> # 保存截屏到手机
adb pull /sdcard/screen.png # 下载截屏文件到本地
```

## 使用方法(仅限于Java版) 
1. Android Studio 自带 adb 即可，一般位于 /Users/mac/Library/Android/sdk/platform-tools
2. 打开安卓手机的usb调试模式并授权连接的电脑
3. 打开微信跳一跳，并**点击开始**
4. 用终端打开adb，并执行一下adb shell，确认adb已经连接上手机后输入exit离开adb shell
5. 输入命令
```
5. 输入命令
java -jar your jar's name.jar -a <your adb path>
```

### 说明
# 参考

<https://github.com/easyworld/PlayJumpJumpWithMouse>

# TODO

Kotlin
