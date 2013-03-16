---
layout: yi
title: 如何把你的谷歌Nexus手机或平板刷成Ubuntu Touch OS操作系统
tags: ['Nexus', 'Ubuntu Touch OS']
description: Ubuntu Touch手机操作系统预览版已经对外发布，可以从官方网站上下载。这个Ubuntu Touch系统可以成功的安装到谷歌的Nexus安卓设备上。早期预览版并不能让你的手机设备具有所有的功能，但一些基本的功能都有。你可以打电话，收发短信，连接无线网络，使用前置和后置摄像头，以及使用shell和一些核心应用。
yi_author: Aqee
yi_toa: Aamir Usman
yi_yan: 外刊IT评论网
yi_url: http://www.aqee.net/ubuntu-tguide-to-install-ubuntu-touch-os-on-nexus-android-devices/
---

<img alt="" src="http://www.aqee.net/wordpress/wp-content/uploads/2013/03/ubuntu-android-nexus-620x350.jpg">

Ubuntu Touch手机操作系统预览版已经对外发布，可以从官方网站上下载。这个Ubuntu Touch系统可以成功的安装到谷歌的Nexus安卓设备上。早期预览版并不能让你的手机设备具有所有的功能，但一些基本的功能都有。你可以打电话，收发短信，连接无线网络，使用前置和后置摄像头，以及使用shell和一些核心应用。

你可以把下列设备刷成Ubuntu Touch OS操作系统：

*   Google Nexus
*   Nexus 4
*   Nexus 7
*   and Nexus 10

把谷歌Nexus设备刷成Ubuntu系统总共需要三个步骤：

*   安装刷机软件程序
*   解锁并设置好你的Nexus设备
*   安装Ubuntu Touch OS

#### 第一步：安装刷机软件程序

下面的步骤是说明如何将刷机程序安装到你的桌面电脑上。

首先在你的/etc/apt/sources.list文件中加入Ubuntu Touch PPA文件源，做法：

	sudo add-apt-repository ppa:phablet-team/tools

然后：

	sudo apt-get update
	sudo apt-get install phablet-tools android-tools-adb android-tools-fastboot

#### 第二步：解锁并设置好你的Nexus设备

这一步可以分成两小步。

第二步(A)解锁设备：如果你的设备已经解锁，可以略过此步。否则，按照下面的步骤解锁root。

*   关机。
*   通过同时按住电源键、音量按钮的+端和-端。一直按着，直到你看到一个肚皮朝上的安卓图像出现。
*   将设备连接上电脑，在电脑上打开命令行窗口，输入下面的命令：


		fastboot oem unlock


*   接受条款，继续。

第二步(b)设置你的设备：

设备解锁后，重新启动。在“开发者选项”里把你的设备设置成USB调试模式。

nexus-4-debugging

下面是针对不同的安卓版本的不同做法：

<img alt="" src="http://www.aqee.net/wordpress/wp-content/uploads/2013/03/nexus-4-debugging.jpg">

*   Android 4.0：到“设置”里打开USB调试选项(设置 > 系统 > 开发者选项 > USB调试)。
*   Android 4.1或4.2：到“设置”里，“关于手机/平板”，在“版本号”上连续点击7次，然后到“开发者选项”里激活“USB调试”(设置 > 开发者选项 > USB调试)
*   Android 4.2.2：你需要接受一个host key，如果你已经安装了adb，这样做：

在你的电脑上-> adb kill-server; adb start-server

现在把你的手机/平板连接上电脑。会弹出一个信息框。接受host key。

#### 第三步：刷Ubuntu Touch系统

在电脑上打开命令窗口，运行如下命令：

	phablet-flash -b

你会被问到是否接受改变，输入“yes”。这样之后Ubuntu系统就会安装到你的设备上。完成了这一步，当你重启时，系统就是Ubuntu操作系统了。

提示：如果你觉得这个系统不太适合你，你可以下载相应的Android image 文件，把系统重新刷回安卓。

免责声明：这个指导只做研究用。我们不对任何操作中产生的事故承担任何责任。