# 锁屏应用

这是一个Android锁屏应用，可以在锁屏界面显示全屏的风景图片和时间。

## 功能特性

- 全屏风景背景显示
- 实时时间显示
- 日期显示
- 点击屏幕解锁
- 前台服务保持运行

## 项目结构

```
app/
├── src/main/
│   ├── java/com/example/lockscreen/
│   │   ├── MainActivity.kt          # 主Activity
│   │   ├── LockScreenActivity.kt    # 锁屏Activity
│   │   └── LockScreenService.kt     # 锁屏服务
│   ├── res/
│   │   ├── layout/
│   │   │   ├── activity_main.xml
│   │   │   └── activity_lock_screen.xml
│   │   ├── drawable/
│   │   │   └── landscape_background.xml
│   │   └── values/
│   │       ├── strings.xml
│   │       ├── colors.xml
│   │       └── themes.xml
│   └── AndroidManifest.xml
```

## 使用方法

1. 编译并安装应用到Android设备
2. 打开应用
3. 点击"启动锁屏"按钮
4. 应用将启动前台服务
5. 锁屏界面会显示全屏风景背景和时间
6. 点击屏幕可以解锁

## 权限说明

应用需要以下权限：
- `DISABLE_KEYGUARD`: 禁用系统锁屏
- `WAKE_LOCK`: 保持屏幕唤醒
- `SYSTEM_ALERT_WINDOW`: 显示系统级窗口
- `FOREGROUND_SERVICE`: 运行前台服务
- `POST_NOTIFICATIONS`: 发送通知

## 自定义背景

要更换背景图片，可以：
1. 将图片文件放在 `app/src/main/res/drawable/` 目录下
2. 修改 `activity_lock_screen.xml` 中的 `android:background` 属性
3. 或者修改 `landscape_background.xml` 中的渐变颜色

## 注意事项

- 此应用需要Android 7.0 (API 24) 或更高版本
- 某些设备可能需要手动授予权限
- 建议在测试设备上运行，避免影响日常使用

## 构建说明

1. 确保已安装Android Studio
2. 打开项目
3. 同步Gradle文件
4. 构建并运行应用 