# VideoSaver
在iPhone上看到一段有趣的视频，想要把它下载到照片里收藏，是件麻烦的事。iOS不支持文件下载，而视频网站为了保护自己的内容，只在自己的App里提供缓存功能。所以我开发了VideoSaver，一个简单易用的Safari视频下载插件。

它的原理很简单：当Safari载入网页后，插件可以运行自定义的JS，这样我们就可以获得网页中的视频地址，轻松下载到想要保存的地方。

VideoSaver已在Github开源，你可以通过Mac下载，用Xcode编译到你自己的iPhone、iPad上。`注：由于 VideoSaver在数据传输上利用了AppGroup技术，免费的开发者账号将无法使用` 请在编译时创建并替换为你的App Group ID。

###插件###
VideoSaver的主要功能在于它的插件。当安装到iPhone 、iPad后，请先在Safari的插件管理中打开VideoSaver。

<img src='https://github.com/nevercry/VideoSaver/blob/gh-pages/images/videoSaverExtension.gif' width='480px'>

在项目的 `VideoExtension` 目录下，有个名为 `MyJSFile.js` 的文件，插件通过它来操作当前网页的DOM。你可以在此对特定的视频网站做自定义解析，可以利用Mac上的Safari Web Inspector 查看iPhone上的网页源码进行调试。具体方式和工具可以参考：[WWDC 2014 Session 512](https://developer.apple.com/videos/play/wwdc2014/512/) 。

###如何使用###
用Safari打开视频网页，确认视频能够播放，点击Safari分享图标，使用插件下载。

<img src='https://github.com/nevercry/VideoSaver/blob/gh-pages/images/videoSaverHowToUse_1.gif' width='560px'>

你可以选择直接下载视频，也可以点击右上角的 `存储` ，将视频链接保存到应用内以便稍后下载。

<img src='https://github.com/nevercry/VideoSaver/blob/gh-pages/images/videoSaverHowToUser_2.gif' width='560px'>

当你在应用内下载收藏的视频，可以切换到其他应用，下载任务将在后台继续进行。VideoSaver支持视频循环播放，iPad版支持画中画，多任务。

<img src='https://github.com/nevercry/VideoSaver/blob/gh-pages/images/videoSaverPiP.gif' width='750px'>

原生支持的视频网站有*Youtube、 Gfycat、Imgur、哔哩哔哩、秒拍*等等，大部分提供**mp4**视频的网页都可以解析到视频地址。 

###影签###

<a href='https://itunes.apple.com/cn/app/videomarks/id1123317863?l=en&mt=8'><img src="https://devimages.apple.com.edgekey.net/app-store/marketing/guidelines/images/badge-download-on-the-app-store-cn.svg" alt=""></a>

由于版权问题VideoSaver无法上架App Store，我去掉了VideoSaver的下载功能，只提供视频网址解析与收藏的服务，改名为 VideoMarks（影签）现已上架。你可以搭配强大的Workflow，完成下载的需求。当然影签也可以作为你的视频书签，记录你感兴趣的视频网址。











##English:

VideoSaver is a simple tool for Safari to download mp4 video on iOS devices. It provides a safari action extension, when the video webpage has loaded, it can run some custom js to fetch the mp4 video link, then you can download the video file either in VideoSaver or in Photos.

Now VideoSaver is open source on Github. You can build it using your Mac with Xcode to your iPhone and iPad. It requires your have Paid Developer Account to run it, because you need to create your own App Group ID which is not available for free one.

###Extension

The most important component of VideoSaver is the Safari extension. When your install the app to the iPhone,iPad make sure you enable the app's extension in Safari.

There is a file named `MyJSFile.js` in the directory `VideoExtension` of the project, you can actually customize it to manipulate the webpage DOM. You can write your custom parse logic code for the specific video site. Use the Safari Web Inspector on your Mac, to lookup the source code of your iPhone webpage, and to do whatever your want. More detail: [WWDC 2014 Session 512](https://developer.apple.com/videos/play/wwdc2014/512/)

###How To Use

Use Safari to open the video webpage, make sure the video can play. Tap the Safari action icon, use the app's extension to download.

You can download video directly, or just save the link to the app for later downloading.

When you download video later in the app, you can switch to other apps, the downloading tasks will continue in the background. VideoSaver supports playing video on loop, the iPad version supports Picture in Picture, multitasking.

Support video download sites included: Youtube,Gfycat,Imgur,bilibili,miaopai,etc..

###VideoMarks 

<a href='https://itunes.apple.com/cn/app/videomarks/id1123317863?l=en&mt=8'><img src="https://devimages.apple.com.edgekey.net/app-store/marketing/guidelines/images/badge-download-on-the-app-store.svg" alt=""></a>

For piracy reason, VideoSaver could't be downloaded from App Store. So I removed the download feature of it, and rename the App Store Version as VideoMarks, you could extend it's ability with the powerful of Workflow. Maybe use it as the video bookmark app.

###Authors

Yang Shengfu (@nevercry)

###Support or Contact 

Having trouble with VideoSaver? Feel free to contact me.  

Email: nsysfmac#gmail.com

Twitter: nevercry




