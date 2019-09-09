在命令行，我们可以安装gradle或者直接使用Aandroid studio 提供的Gradle wrraper执行构建命令。Gradle wrraper包含了了gradlew脚本和gradlew.bat脚本。前者给UNIX使用，后者给Windows使用。脚本依赖gradle.wrapper.properties的配置，在脚本中调用gradle-wrapper.jar 来实现构建。

##### gradle.wrapper.properties各项配置含义

- distributionUrl：wrapper会下载安装的gradle版本地址。
- zipStoreBase与zipStorePath：gradle发行版的压缩包会下载到zipStoreBase下的zipStorePath目录下
- distributionBase与distributionPath：gradle压缩包解压之后存放的地址。base是根目录，path是子目录

##### 构建命令
- ./gradlew build ：构建
- ./gradlew lint assembleDebug 通过空格分隔来执行多个任务
- ./graldew assembleDebug -x lindebug ：通过-x 标志来表示不执行某一个任务
- 