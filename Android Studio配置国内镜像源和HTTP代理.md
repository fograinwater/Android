# Android Studio配置国内镜像源和HTTP代理

### 一、配置国内镜像源/依赖库

#### 1.1 打开项目的`setting.gradle.kts`文件

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/win11/image-20231213152538637.png" alt="image-20231213152538637" style="zoom:60%;" />

#### 1.2 根据需要填入仓库地址

##### 1.2.1 新版`kotlin`文件

```kotlin
maven { url=uri ("https://www.jitpack.io")}
maven { url=uri ("https://maven.aliyun.com/repository/releases")}
maven { url=uri ("https://maven.aliyun.com/repository/google")}
maven { url=uri ("https://maven.aliyun.com/repository/central")}
maven { url=uri ("https://maven.aliyun.com/repository/gradle-plugin")}
maven { url=uri ("https://maven.aliyun.com/repository/public")}
```

- 示例

```kotlin
pluginManagement {
    repositories {
        maven { url=uri ("https://www.jitpack.io")}
        maven { url=uri ("https://maven.aliyun.com/repository/releases")}
        maven { url=uri ("https://maven.aliyun.com/repository/google")}
        maven { url=uri ("https://maven.aliyun.com/repository/central")}
        maven { url=uri ("https://maven.aliyun.com/repository/gradle-plugin")}
        maven { url=uri ("https://maven.aliyun.com/repository/public")}

        google()
        mavenCentral()
        gradlePluginPortal()
    }
}
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        maven { url=uri ("https://www.jitpack.io")}
        maven { url=uri ("https://maven.aliyun.com/repository/releases")}
        maven { url=uri ("https://maven.aliyun.com/repository/google")}
        maven { url=uri ("https://maven.aliyun.com/repository/central")}
        maven { url=uri ("https://maven.aliyun.com/repository/gradle-plugin")}
        maven { url=uri ("https://maven.aliyun.com/repository/public")}


        google()
        mavenCentral()
    }
}

rootProject.name = "HelloWorld"
include(":app")
```

##### 1.2.2 旧式gradle文件

```
maven { url "https://jitpack.io" }        
maven { url 'https://maven.aliyun.com/repository/releases' }
maven { url 'https://maven.aliyun.com/repository/jcenter' }
maven { url 'https://maven.aliyun.com/repository/google' }
maven { url 'https://maven.aliyun.com/repository/central' }
maven { url 'https://maven.aliyun.com/repository/gradle-plugin' }
maven { url 'https://maven.aliyun.com/repository/public' }
```

- 示例：

```
pluginManagement {
    repositories {
        maven { url "https://jitpack.io" }
        maven { url 'https://maven.aliyun.com/repository/releases' }
        maven { url 'https://maven.aliyun.com/repository/jcenter' }
        maven { url 'https://maven.aliyun.com/repository/google' }
        maven { url 'https://maven.aliyun.com/repository/central' }
        maven { url 'https://maven.aliyun.com/repository/gradle-plugin' }
        maven { url 'https://maven.aliyun.com/repository/public' }
        google()
        mavenCentral()
        gradlePluginPortal()
    }
}
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        maven { url "https://jitpack.io" }
        maven { url 'https://maven.aliyun.com/repository/releases' }
        maven { url 'https://maven.aliyun.com/repository/jcenter' }
        maven { url 'https://maven.aliyun.com/repository/google' }
        maven { url 'https://maven.aliyun.com/repository/central' }
        maven { url 'https://maven.aliyun.com/repository/gradle-plugin' }
        maven { url 'https://maven.aliyun.com/repository/public' }
        google()
        mavenCentral()
    }
}
rootProject.name = "EasyUtils"
include ':app'
```

#### 1.3 点击“Sync Now”按钮，同步Gradle配置

#### 1.4 注意事项

- `pluginManagement`和`dependencyResolutionManagement`里面的`repositories`都需要填写
- 不同的`gradle`文件的`url`格式不一样





### 二、配置HTTP代理

#### 1.1 代理服务器的作用

- 内容缓存：缓存经常访问的网页和数据，当再次访问时可以直接从代理服务器获取，加快访问速度。
- 绕过限制：某些国外源在国内访问的速度极慢，通过代理可以绕过限制，实现跨地域访问。
- 安全性：匿名浏览，数据加密

#### 1.2 国内常用的代理服务器

1、东软信息学院

```
mirrors.neusoft.edu.cn     端口：80
```

2、北京化工大学

```
ubuntu.buct.edu.cn/ubuntu.buct.cn  端口：80
```

3、中国科学院开源协会

```
mirrors.opencas.cn (mirrors.opencas.org/mirrors.opencas.ac.cn)    端口：80
```

4、上海GDG镜像服务器

```
sdk.gdgshanghai.com   端口：8000
```

5、电子科技大学

```
mirrors.dormforce.net  端口：80
```

#### 1.3 步骤

- 打开左上角`File` ==> `setting` ==> `HTTP Proxy` 

- 然后填入镜像地址

  ```
  腾讯： https://mirrors.cloud.tencent.com/AndroidSDK/
  阿里： https://mirrors.aliyun.com/android.googlesource.com/
  ```

- `Apply` ==> `OK`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/win11/image-20231213145008865.png" alt="image-20231213145008865" style="zoom: 50%;" />



### 三、可能遇到的问题

##### 问题1

```
Plugin [id: ‘com.android.application‘, version: ‘x.x.x‘, apply: false] was not found ......
```

**解决办法**

- 查看一下你的gradle对应的JDK版本是否过低，目前8.0版本对应的是JDK17.

- 检验cmd输入`java --version`查看的版本是否与下载的版本一致

- 查看环境变量中是否有其他版本的 `jdk` 版本

- 查看`android studio`的`gradle`是否使用的相同版本的`jdk`）

  <img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/win11/image-20231213153823380.png" alt="image-20231213153823380" style="zoom:70%;" />

  

  <img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/win11/image-20231213153755412.png" alt="image-20231213153755412" style="zoom:70%;" />

  

  <img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/win11/image-20231213153732489.png" alt="image-20231213153732489" style="zoom:50%;" />



##### 问题2

- 前面配置了多次代理，后面不论怎么配置都无法配置成功

**解决办法**

- 打开`C:\Users\用户名\.gradle`文件夹下的`gradle.properties`文件，直接删掉/注释掉最后几行的代理信息

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/win11/image-20231213154714065.png" alt="image-20231213154714065" style="zoom:60%;" />



##### 问题3

```
Android Studio Unexpected tokens (use ； to separate expressions on the same line)
```

**原因：**

- Android Studio 更新到最新的版本之后，gradle工程目录结构发生改变

**解决办法：**

- 将`setting.gradle`文件中的仓库从旧式格式改为新式`kotlin`格式：

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/win11/image-20231213154932363.png" alt="image-20231213154932363" style="zoom:70%;" />

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/win11/image-20231213155021995.png" alt="image-20231213155021995" style="zoom:60%;" />

- Eg：

```kotlin
maven { url=uri（"https://www.jitpack.io")}
```



