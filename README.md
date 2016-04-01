#一套优雅的IM实现方案：UI篇

**新建项目交流群：533793277**

##前言
从事ios开发以来， 一直混迹于微博，简书，gitHub上， 技术上的增长一直很大一部分是从中受益，但自己鲜有文墨或开源项目贡献，并不是自己文笔太差，逻辑不够灵活，(ˇˍˇ) 想～在上大学时标准文青一枚，各种挥毫墨墨，但进入工作岗位后很多闲情逸致直接被打磨没了。不扯了，入正题。

IM的这套业务逻辑，加上ui的实现，精细起来其实是一件不容易的事情在环信，融云这些第三方厂商还没崛起之前，并不是像如今是个app都轻松接入IM这般，通过第三方接入IM会省去很多麻烦，不用搭建IM服务器，不用管语音、视频怎么压缩、降噪和加密，如何解决高并发下的网络延迟等等问题，这些第三方不仅提供底层IM通讯的API接口给开发者调用，他们竟然还统一都贴心的提供了与通讯接口融合在一起的UI页面，包括注册登陆页面、通讯录、历史聊天记录、单聊群聊等等界面，只有你想不到，没有他们做不到。这样做Im，想不会都难......


事情又要说道一个不太相关的方面，会接入环形等第三方的人不一定会IM整套业务逻辑，在这些厂商帮助下，你的接入不用过多去关注整个业务以及ui的整个实现，一个项目下来，技术进步可能微乎其微。所以，如果正在要了解Im这套，还是需要抛弃这些第三方。


这下可以说说我这个项目。
我是本着开源来做这个项目的，大致规划会分几期来做，前期（当前阶段）就是搭建好大致框架，精细好聊天这套UI,定制好所有业务，ui相关的接口；后期是接入xmpp，大致融合好相关的业务。

### 已完成
1. 聊天相关的所有ui:
    - 自定义键盘：可实现文本，emoij表情，自定义gif表情发送
2.  可模拟发送以下消息类型：
      -  文本消息
      -  音频消息
      -  视频消息
      -  照片消息
      -  位置消息
      
 3. 可模拟接收消息：接收消息类型与发送一致。
  
 3. 定制了一系列接口：
     - im底层的接口：接入webSock，或xmpp。
     - 媒体消息类型处理的接口：转码或者其他的展现形式
  
 5.  设计了消息模型。
 
 
### 未完成,待完成
  1. IM通讯模块的接入；
  2. ui更精细化；
  3. 未发现的bug待解决；
  3. 性能调优。



  
### 效果图
   
  ![](http://7xrwki.com1.z0.glb.clouddn.com/gifSmall1.gif)

![](http://7xrwki.com1.z0.glb.clouddn.com/gifSmall2.gif)

   ![](http://7xrwki.com1.z0.glb.clouddn.com/Simulator%20Screen%20Shot%202016%E5%B9%B43%E6%9C%8831%E6%97%A5%20%E4%B8%8B%E5%8D%889.17.11.png)
   ![](http://7xrwki.com1.z0.glb.clouddn.com/Simulator%20Screen%20Shot%202016%E5%B9%B43%E6%9C%8831%E6%97%A5%20%E4%B8%8B%E5%8D%889.17.25.png)
   ![](http://7xrwki.com1.z0.glb.clouddn.com/Simulator%20Screen%20Shot%202016%E5%B9%B43%E6%9C%8831%E6%97%A5%20%E4%B8%8B%E5%8D%889.17.27.png)
   ![](http://7xrwki.com1.z0.glb.clouddn.com/Simulator%20Screen%20Shot%202016%E5%B9%B43%E6%9C%8831%E6%97%A5%20%E4%B8%8B%E5%8D%889.17.29.png)
   ![](http://7xrwki.com1.z0.glb.clouddn.com/Simulator%20Screen%20Shot%202016%E5%B9%B43%E6%9C%8831%E6%97%A5%20%E4%B8%8B%E5%8D%889.17.32.png)

 
 
 
 
 
 
  
 至于项目的细节，感兴趣的同学可以下载项目，请在真机上体验，如果后期有需要，我会画出项目相关的类图。
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
      
      
      
