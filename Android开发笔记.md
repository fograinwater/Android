# Android开发笔记

#### XML文件中的命名空间

[Android中XML的命名空间、自定义属性-CSDN博客](https://blog.csdn.net/xx326664162/article/details/63254622#:~:text=Android中常见的命名空间 1 1、android xmlns%3Aandroid%3D” http%3A%2F%2Fschemas.android.com%2Fapk%2Fres%2Fandroid ” 在Android布局文件中我们都必须在根元素上定义这样一个命名空间%2C接下来对这行代码进行逐一讲解： xmlns,3、自定义命名空间 如果使用DataBinding 会在xml用到 app属性，其实这是个自定义命名空间。 xmlns%3Aapp%3D” http%3A%2F%2Fschemas.android.com%2Fapk%2Fres-auto ” )

xml文件中的命名空间如下

```xml
```

作用

拓展

自定义命名空间



#### 单位

dp（density-independent pixel）：像素点



##### layout_gravity和gravity的区别

- layout_gravity指的是该**组件相对于父容器**的布局
- gravity指的是该**组件的内容在该组件内**的布局

