# Android Studio安装和配置

### 关于Android Studio

Android Studio是谷歌推出的一个Android集成开发工具，基于IntelliJ IDEA. 类似 Eclipse ADT，Android Studio 提供了集成的 Android 开发工具用于开发和调试。Android Studio能够在Linux、Windows、macOS上运行，支持Java、Kotlin、Flutter等语言开发。



在IDEA的基础上，Android Studio 提供：

- 基于Gradle的构建支持
- Android 专属的重构和快速修复
- 提示工具以捕获性能、可用性、版本兼容性等问题
- 支持ProGuard 和应用签名
- 基于模板的向导来生成常用的 Android 应用设计和组件
- 功能强大的布局编辑器，可以让你拖拉 UI 控件并进行效果预览



### 安装的前置准备

##### 1.已经完成Java环境配置

##### 2.保证网络通畅，否则后续下载会很慢



### 一、Android Studio下载

##### 1.进入官网的下载页面：[Download Android Studio & App Tools - Android Developers (google.cn)](https://developer.android.google.cn/studio/)，点击`Download Android Studio Flamingo`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230530235139512.png" alt="image-20230530235139512" style="zoom: 100%;" />



##### 2.下拉直接跳过提示信息，直到页面最后

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230530235051212.png" alt="image-20230530235051212" style="zoom: 50%;" />



##### 3.点击`I have read and agree with the above terms and conditions`，然后点击`Download`

![image-20230530234902986](https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230530234902986.png)





### 二、Android Studio安装

##### 1.双击刚刚下载的文件

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531083956480.png" alt="image-20230531083956480" style="zoom: 67%;" />



##### 2.选择`Android Virtual Device`即可，然后点击`Next`

- Android Studio：

  Android Studio是一个全功能的集成开发环境（IDE），专门用于Android应用程序的开发。它提供了丰富的开发工具、调试器、代码编辑器和设计工具，使开发者能够创建、编写、调试和测试Android应用程序。Android Studio还提供了项目管理、版本控制、构建系统和应用程序发布等功能。

- Android Virtual Device (AVD)：

  Android Virtual Device是一个模拟器，允许在计算机上模拟Android设备。AVD允许开发者在模拟的Android环境中运行和测试应用程序，而无需实际的物理设备。开发者可以使用AVD来模拟不同的Android设备，包括不同的屏幕尺寸、分辨率、操作系统版本和硬件特性，以便在不同的环境下测试应用程序的适配性和功能。

因为我们之前安装了IDEA，可以代替Android Studio。但是如果想用Android Studio来进行Android开发也是可以的。

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084031947.png" alt="image-20230531084031947" style="zoom: 67%;" />



##### 3.选择安装位置（建议不要安装在C盘），然后点击`Next`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084046658.png" alt="image-20230531084046658" style="zoom:67%;" />



##### 4.点击`Install`即可

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084132561.png" alt="image-20230531084132561" style="zoom:67%;" />



##### 5.等待`Extract`完成，点击`Next`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084206243.png" alt="image-20230531084206243" style="zoom:67%;" />



##### 6.点击`Finish`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084317203.png" alt="image-20230531084317203" style="zoom:67%;" />



##### 7.选择`Do not import directory`，然后点击`OK`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084516398.png" alt="image-20230531084516398" style="zoom:80%;" />



##### 8.进入了欢迎界面，是否发送使用的信息给谷歌，点击`Don't send`即可

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084545798.png" alt="image-20230531084545798" style="zoom: 80%;" />



##### 9.然后提示无法访问Android SDK附加组件列表，这里点击`Cancel`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084627874.png" alt="image-20230531084627874" style="zoom:67%;" />



##### 10.接下来这个图片是告诉你Android Studio能做的事情：手机，穿戴设备，TV，还有智能设备等，点击 `Next` 

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084715774.png" alt="image-20230531084715774" style="zoom:67%;" />



##### 11.然后选择`Custom`（自定义）安装模式（如果选择`Standard`安装模式会默认把你的SDK下载放在C盘，到时候你的C盘就炸了）

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084838373.png" alt="image-20230531084838373" style="zoom:67%;" />



##### 12.然后就进入编了译工程目录选项，系统默认选择安装目录下的jre文件夹，此时保持默认即可，点击`Next`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531084909491.png" alt="image-20230531084909491" style="zoom:67%;" />



##### 13.进入UI主题选择界面，根据自身喜好进行黑色背景或白色背景，然后点击`Next`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531085006264.png" alt="image-20230531085006264" style="zoom:67%;" />



##### 14.然后进行SDK组件的安装和路径的选择，根据实际需求进行组件下载，如果内存不紧张建议全部下载，当然，后期也可以在使用时再进行下载

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531085752154.png" alt="image-20230531085752154" style="zoom:67%;" />



**【这里选择SDK的安装路径时可能会出现两种错误】：**

- 一种是SDK安装在Android Studio目录导致的，此时你需要在 Android Studio 的安装目录外新建一个文件夹用来存放SDK

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531085937310.png" alt="image-20230531085937310" style="zoom:67%;" />



- 另一种是安装路径包含空格，此时你需要选择或创建一个不包含空格的路径：

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531090009633.png" alt="image-20230531090009633" style="zoom:67%;" />

路径修改后，报错消失，点击`Next`



##### 15.然后再点击`Next`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531090305060.png" alt="image-20230531090305060" style="zoom:67%;" />



##### 16.确认信息后点击`Next`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531090322304.png" alt="image-20230531090322304" style="zoom:67%;" />



##### 17.点击左侧目录的两个选项，均选择`Accept`后，点击`Finish`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531090444184.png" alt="image-20230531090444184" style="zoom:67%;" />



<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531090516046.png" alt="image-20230531090516046" style="zoom:67%;" />



##### 18.然后等待

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531090602281.png" alt="image-20230531090602281" style="zoom:67%;" />



##### 19.下载完成后点击`Finish`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531091227557.png" alt="image-20230531091227557" style="zoom:67%;" />



##### 20.点击创建`New Project`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531091304007.png" alt="image-20230531091304007" style="zoom:67%;" />



##### 21.点击`'Empty Activity'`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531091436281.png" alt="image-20230531091436281" style="zoom:60%;" />



##### 22.填写项目信息，如果`Save location`在C盘的话这里可以修改一下项目保存路径，信息修改填写完成后点击`Finish`

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531091623185.png" alt="image-20230531091623185" style="zoom:60%;" />



##### 23.然后进入下面这个界面就会开始创建这个项目并下载一些配置文件

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531091757140.png" alt="image-20230531091757140" style="zoom:40%;" />



##### 24.下载完成后可以点击右上角绿色的小三角运行一下他给出的测试代码

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531092103826.png" alt="image-20230531092103826" style="zoom:40%;" />



##### 25.运行结果如下图

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230531092632387.png" alt="image-20230531092632387" style="zoom: 40%;" />

