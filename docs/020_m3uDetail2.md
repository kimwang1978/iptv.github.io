##  新手入门系列： m3u格式之EPG（电视节目预告）

>>公众号文章迁移至此。

上篇 [新手入门系列： m3u直播源格式之详解](./docs/019_m3uDetail.md) 在M3U文件中有个参数：x-tvg-url
```javascript
#EXTM3U x-tvg-url="https://xxx.xxxx.com/xxx.xml"
```
这就是传说中的 **EPG（电视节目预告）** 参数。

**EPG：** Electronic Program Guide首字母缩写，直译“电子节目指南”，通俗易懂地讲在我们直播源中就是“电视节目预告”。播放节目内容时显示的电视节目表信息，可以帮助用户快速查看每个频道的节目安排。M3U文件本身并不直接包含EPG数据，而是通过链接外部XML文件或指定EPG URL来实现，上面提到的x-tvg-url参数就是来实现这个的。

仅仅配上 **x-tvg-url** 参数是不够的，在上篇小作文中另外还有两个参数与EPG相关，在EPG信息中有大量频道的预告信息，这样就会出现这些信息如何与之对应频道正确匹配的问题，于是就引出了 **tv-id** 和 **tv-name** 两个参数。

>**tvg-id：** EPG数据的频道ID，用于将M3U列表中的频道与EPG数据对接。通常这个ID在EPG文件（通常是XML文件）中也会有相应的定义。 

>**tvg-name：** 该字段通常用于存储频道的名称，与EPG文件中的频道名称匹配，用于显示节目时的名称显示。

这两个参数都可以与EPG指向进行匹配，当两者都指定发生冲突时怎么办，其实这里两个匹配上还是有优先级的：一般来说，播放器会优先使用tvg-id字段来匹配EPG信息，因为tvg-id是一个唯一标识符，而tvg-name则更多用于显示名称。好像更推荐tvg-id，但是本号更习惯用tvg-name

### 简单示例

假设EPG XML文件中定义如下：
```xml
<tv>   
  <channel id="channel123"> 
    <display-name>Channel One</display-name>
  </channel> 
</tv>
```
M3U文件中可以如下配置：
```javascript
#EXTINF:-1 tvg-id="channel123" tvg-name="My Channel One" tvg-logo="http://example.com/logo.png", My Channel One http://stream-url.com/stream.m3u8
```

**tvg-url** 在M3U文件中可以每个频道中分别设定也可以如文章开头所示使用一个统一的EPG信息。也可以同时设定多个EPG，逗号分隔开，但是在设定之前你需要确认你所使用的 **播放器是否支持多个EPG源** ，而且多个EPG源的情况下优先度根据播放器可能会有所不同，有安装文件先后加载顺序，也有合并后安装tv-id优先原则匹配。

**EPG源示例：**

    https://epg.112114.xyz/pp.xml 
    https://live.fanmingming.cn/e.xml 
    https://assets.livednow.com/epg.xml


## 获取更多，欢迎关注公众号：百宝箱箱
![image](../assets/GongZhongHao.png)

[返回](..)
