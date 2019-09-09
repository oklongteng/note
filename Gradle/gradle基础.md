### Gradle构建文件

##### 1.setting.gradle

##### 2.build.gradle(project)

buildScrip {/**/} :gradle构建脚本身所需依赖

```groovy
buildsScrip{
  repositories{
    jcenter()
  }
  classpath "com.android.tools.build:gradle:2.3.0"
}
```

allProjects{/**/} :项目本身所需依赖

```groovy
allProjects{
  resitories {
    jcenter()
  }
}
```

##### 3 build.gradle（module）

- compileSdkVersion:指定编译环境
- buildToolsVersion:指定编译工具版本
- minSdkVersion:支持的最小的Android SDK版本
- targetVersion：the main way Android provides forward ompatbility(Android实现先后兼容的主要手段)。随着Android 系统的升级，某些API的行为可能发生变化。但是只要targetSdkVersion不变，即使这个APK安装在新的系统上，其行为还是和老的系统保持一致。Android系统在执行系统API的时候，会获取targetSdkVersion执行相应的行为。