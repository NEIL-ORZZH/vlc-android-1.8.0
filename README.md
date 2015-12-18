因为采用tar.gz压缩格式, 文件比较大,暂时放到百度网盘,以后更新到这里 下载地址是: http://pan.baidu.com/s/1dEjE6rR

this is vlc-android version all source code .compiled by LanSoSdk team.
compile step by :https://wiki.videolan.org/AndroidCompile#Requirements
in codes, we add some MediaPlayer motheds, so you can calling libvlc like this:
	
							mMediaPlayer = new MediaPlayer(this);
        	  	mMediaPlayer.setVideoView(mSurfaceView); 
        	  	mMediaPlayer.setOnVideoSizeChangedListener(this);
        	  	mMediaPlayer.setDataSource(mUri,isSwCodec);
             	mMediaPlayer.setEventListener(mMediaPlayerListener);
             	mMediaPlayer.setOnHardwareAccelerationErrorListener(this);
              mMediaPlayer.play();

	belove demo in VideoPlayerActivity2.java. 	
	Hope Enjoy.
-------------------------->
为了大家更好的调用,我们对MediaPlayer类增加了一些代码, 这样大家可以直接参考VideoPlayerActivity2.java中的写法, 来使用vlc-android.

编译完全按照:
		https://wiki.videolan.org/AndroidCompile#Requirements 的操作步骤进行.
	(如果您是初学者,建议新建一个虚拟机,完全编译)

此代码是LanSoSdk编译后,完全没有clean的代码,编译过程中的各种配置文件,.o文件都是存在的.
如果您想很快的编译,请设置和我们完全一致的路径,包括ubuntu的用户名.文件路径是/home/sno/vlc_android17/xxx源代码.

	
我们的编译过程
   系统win7中安装虚拟机,里面装ubuntu12.04(64位)(同事用ubuntu14.04一样可以编译成功).
  各种环境如下(my env is):
   	export JAVA_HOME=/home/sno/android_tools/jdk1.7.0_51
		export JRE_HOME=/home/sno/android_tools/jdk1.7.0_51/jre
		export ANDROID_ABI=armeabi-v7a
		export ANDROID_SDK=/home/sno/android_tools/adt-bundle-linux-x86_64-20140321/sdk
		export PATH=$PATH:$ANDROID_SDK/platform-tools:$ANDROID_SDK/tools
		export ANDROID_NDK=/home/sno/android_tools/ndk/android-ndk-r10e

 
请大家在github的issue中讨论各种遇到的问题,尽量采用英文,以便国外的各种的大牛看到, 一起讨论.

(团队介绍)	
 杭州蓝松科技有限公司.LanSoSdk团队, 专业做多媒体音视频的方案公司.包括视频采集,编辑,编码, 传输,解码,处理,播放等.
   
 由于使用vlc做过多个项目, 以下是我们针对vlc-android做的高级功能,欢迎商务合作.	
 演示地址:https://github.com/LanSoSdk/LanSoSdkPlayDemo
 		
 1,设置视频下载缓冲器大小,设置视频缓冲时长.		
 2,视频截屏,单帧播放.	
 3,视频播放速度可调,任意速度可调.
 4,软硬解自动切换.完全支持软硬解.并软解功能支持NEON指令,多线程解码.
 5,视频录制.	
 6,网络视频支持边播放、边下载功能. 支持快速全速下载.----网络不太好,或使用3G/4G情况下也可以流畅播放.	
 7,网络视频,查看当前缓冲百分比, 查看当前网速.----	
 8,支持对比度, 饱和度,色调,颜色提取,镜像,动态监测,分屏等12种功能,并可定制滤镜效果.  ----类似秒拍,美拍,快手的功能.	
 9,支持左右3D, 红蓝3D播放.	
 10,RTSP做视频直播时的延迟问题(定制).	
 11,RTSP播放时马赛克严重的问题(定制).		
 12,硬件在部分手机上不支持的问题(定制).		
 13,M3U8网络播放时crash的问题(定制).	
 14,解决您项目中遇到的各种视频网络等问题(定制).			
 
 
 
 Emai: support@lansongtech.com, QQ群 235842416; 商务联系1852600324(busy)
