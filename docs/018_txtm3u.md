[返回主页面](..)
## 新手入门系列：txt直播源 vs m3u直播源

>公众号文章迁移至此。

### txt源（txt直播源）

大道至简。一个分组标志位（#genre#），然后就是 **频道名,频道地址** ，没有太多花里胡哨，简单易懂，新手容易上手。格式示例：

```javascript
央视,#genre#
CCTV1,http://example.com/cctv1.m3u8
CCTV2,http://example.com/cctv2.m3u8
CCTV3,http://example.com/cctv3.m3u8

卫视,#genre#
东方卫视,http://example.com/dfws.m3u8
湖南卫视,http://example.com/hnws.m3u8
江苏卫视,http://example.com/jsws.m3u8
```

### m3u源（m3u直播源）

拥有更丰富控制，可以加入台标，控制EPG电视节目清单等。与枯燥的txt源相比能看到熟悉的台标，是不是更有有种亲切感，缺点就是格式配置稍显复杂。格式示例：

```javascript
#EXTM3U

#EXTINF:-1 tvg-id="cctv1" tvg-name="CCTV-1" group-title="CCTV" tvg-logo="https://example.com/cctv1.png",CCTV-1 综合
http://example.com/live/cctv1.m3u8

#EXTINF:-1 tvg-id="cctv5" tvg-name="CCTV-5" group-title="CCTV" tvg-logo="https://example.com/cctv5.png",CCTV-5 体育
http://example.com/live/cctv5.m3u8

#EXTINF:-1 tvg-id="hktv" tvg-name="TVB Jade" group-title="香港台" tvg-logo="https://example.com/tvbjade.png",TVB 翡翠台
http://example.com/live/tvbjade.m3u8

#EXTINF:-1 tvg-id="rthk31" tvg-name="RTHK31" group-title="香港台" tvg-logo="https://example.com/rthk31.png",RTHK31
http://example.com/live/rthk31.m3u8

```

各种播放工具支持各不同，有些两者都支持，可以都试试效果。比较典型播放源播放工具：**TvBox**，**影视仓**，**FongMi**，**派大星直播**，各种魔改版等。手机播放器的话只要集中在安卓系统上，苹果系统由于其系统封闭性和审核严格性App相对较少。Windows桌面系统上 **PotPlayer** 也是支持的，本号比较推荐 **ZyPlayer** 。


### M3U ⇄ TXT 转换工具
>追记：txt格式与m3u格式可以互转。

*   🛠️ [M3U ⇄ TXT 转换](https://convert.iptv365.org) 

## 获取更多，欢迎关注公众号：百宝箱箱
<img src="../assets/GongZhongHao.png" style="max-width:100%; height:auto;">

[返回](..)