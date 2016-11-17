.. _installation:

安装
============

开发Exponent应用你需要两个工具: 一个桌面开发工具还有exponent应用来打开你的app。

桌面开发工具: XDE
-----------------------------

XDE是Exponent Development Environment的缩写, 它包含了所有你需要的依赖组件。

下载地址:
`macOS <https://xde-updates.exponentjs.com/download/mac>`_, `Windows <https://xde-updates.exponentjs.com/download/win32>`_, `Linux <https://xde-updates.exponentjs.com/download/linux>`_.

Linux上的话，运行 ``chmod a+x XDE*.AppImage`` 然后 ``./XDE*.AppImage`` 打开。

Exponent应用: 支持iOS和Android
--------------------------------------------

Exponent应用好比一个应用浏览器(用Exponent开发的应用)。
当你在XDE上启动你的项目，它会生成一个唯一的开发URL, 然后你可以在Exponent应用上输入这个URL进入你的应用, 设备或者模拟器都支持。

在设备上运行
^^^^^^^^^^^^^^

`在Play Store上下载(Android 4.4+) <https://play.google.com/store/apps/details?id=host.exp.exponent>`_ 或者 `App Store(iOS 8+)下载 <https://itunes.com/apps/exponent>`_

注意: 当你第一次开发应用时，模拟器会自动安装Exponent应用.

iOS 虚拟机
^^^^^^^^^^^^^

安装 `Xcode <https://itunes.apple.com/app/xcode/id497799835>`_. 需要一会儿时间，不如打个盹儿。然后打开配置，点击组件，安装一个虚拟机, `(screenshot). </_static/img/xcode-simulator.png>`_

这时候如果你在XDE里已经打开一个项目，你可以点击 *Open on iOS simulator*, XDE会自动安装Exponent应用到虚拟机，并且在Exponent应用里打开你的应用。

Android 虚拟机
^^^^^^^^^^^^^^^^
`下载 Genymotion <https://www.genymotion.com/fun-zone/>`_ (免费版本), 安装文档: `Genymotion installation guide <https://docs.genymotion.com/Content/01_Get_Started/Installation.htm>`_.

安装好Genymotion后，创建一个虚拟设备 - 我们推荐Nexus 5, Android版本你可以自己选。然后启动虚拟设备。

这时候如果你在XDE里已经打开一个项目, 你可以点击 *Open project in Exponent on Android*, XDE会自动安装Exponent应用到虚拟机，并且在Exponent应用里打开你的应用。

Node.js
--------
单独用Exponent你不需要安装Node.js, 但是当你真正开始开发的时候，你需要安装它.
`下载最新的Node.js <https://nodejs.org/en/>`_.

Watchman
--------

不安装Watchman的话，一些macOS用户会遇到一些问题.
我们推荐你安装它。Watchman会监视文件，一旦文件改变会记录下来，然后触发对应的操作。React Native有用到它。`下载并安装Watchman <https://facebook.github.io/watchman/docs/install.html>`_
