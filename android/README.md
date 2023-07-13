# 构建命令
1. 打包
```
# 项目跟目录下
flutter build apk --release --no-sound-null-safety --no-tree-shake-icons -v
```

# 问题记录

1. gradle与flutter版本问题
```
Gradle 7.4 与flutter_windows_3.3.0-stable 可以
```

2. 打包报错jdk版本不对
```
* What went wrong:
A problem occurred evaluating project ':app'.
> Failed to apply plugin 'com.android.internal.application'.
   > Android Gradle plugin requires Java 11 to run. You are currently using Java 1.8.
      Your current JDK is located in D:\tools2\androidstudio\android-studio-ide-191.5977832-windows\android-studio\jre\jre
      You can try some of the following options:
       - changing the IDE settings.
       - changing the JAVA_HOME environment variable.
       - changing `org.gradle.java.home` in `gradle.properties`.

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 12s
```
解决：按提示配置org.gradle.java.home