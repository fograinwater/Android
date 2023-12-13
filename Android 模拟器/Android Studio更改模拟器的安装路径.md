#### Android Studio更改模拟器安装路径

这篇文章首先介绍为什么要更改模拟器的安装位置，然后给出具体步骤。



#### 1. 为什么需要更改模拟器安装路径

在使用Android Studio开发了一段时间后，你会发现自己的C盘容量突然少了10个G左右。

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230804113102276.png" alt="image-20230804113102276" style="zoom:67%;" />

研究了一下原因，发现Android的模拟器默认直接下载到C盘，而一个模拟器大概就占了10个G！

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230923090850513.png" alt="image-20230923090850513" style="zoom: 70%;" />

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230804113245653.png" alt="image-20230804113245653" style="zoom:67%;" />

所以我们得想办法更改模拟器的安装路径。



#### 2. 步骤

##### 2.1 更改`.android`文件夹的路径

将`C:\Users\用户名\.android`目录下的`.android`的整个文件夹剪切到`Android SDK`的安装目录（可以在`setting`中查看`SDK`的安装路径；如果 `sdk`的存放路径也在C盘，可以点击 `Edit` 进行更改）

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230923091238972.png" alt="image-20230923091238972" style="zoom:50%;" />



<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230912230349363.png" alt="image-20230912230349363" style="zoom: 67%;" />



##### 2.2 新建`AVD`环境变量

新建存放`AVD`的系统环境变量，变量名为`ANDROID_AVD_HOME`，变量值为模拟器存放的位置，这里是`D:\Android_SDK\.android\avd`。

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230912230802955.png" alt="image-20230912230802955" style="zoom:67%;" />

<img src="https://raw.githubusercontent.com/fograinwater/PicGo-img/master/image-20230912230601752.png" alt="image-20230912230601752" style="zoom:67%;" />



##### 2.3 删除原模拟器文件

删除`D:\Android_SDK\.android\avd`中的模拟器文件，因为此时路径更改了，重新打开`Android Studio`无法启动原来的那个模拟器。



##### 2.4 新建模拟器

打开`Android Studio`新建一个模拟器，验证修改是否成功。

- 可以发现此时 `avd` 的存放路径在 `AVD系统环境变量` 所指示的位置

- C盘中仍然有`.android`文件夹，但是里面没有`avd`文件了，但是如果最开始不删除`.android`整个文件夹，模拟器仍然会在C盘中保存文件。



#### 3. 注意事项

- **注：**如果新建系统变量后没有删除默认的存放地址，则以后创建的模拟器仍存放在默认的地址。
- 具体步骤、其他问题也可以参考这篇博客：【[Android Studio 如何修改模拟器的存放路径](https://blog.csdn.net/weixin_43813694/article/details/105337645)】

