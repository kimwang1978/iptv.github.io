[返回主页面](..)
## 新手入门系列： m3u格式之详解

>公众号文章迁移至此。

M3U 文件是一种简单的播放列表格式，用于组织和存储媒体文件或流媒体的 URL 列表。它最初是为音频播放列表设计的，但也适用于视频流和 IPTV 频道。M3U 文件使用纯文本格式，可以很方便地编辑和自定义。

### M3U 文件的基本结构
M3U 文件的每行通常是以下三种类型之一：

*   **文件头：** #EXTM3U，表示该文件是一个扩展 M3U 文件。
*   **信息行：** #EXTINF，描述媒体文件的元数据（如标题、时长等）。
*   **媒体地址：** 通常是媒体文件的 URL（例如 HTTP 地址、RTSP 地址或本地文件路径）。 

### 详细结构
*   文件头 #EXTM3U
M3U 文件的第一行通常是 #EXTM3U，表示该文件是一个扩展 M3U 文件。这一行是可选的，但在 IPTV 使用的 M3U 文件中几乎总是包含这一行。
    ```javascript
    #EXTM3U
    ```

*   信息行 #EXTINF
#EXTINF 是 EXTended INFo 的缩写，它用于提供每个流或媒体文件的元数据，包括持续时间和标题等信息。典型的 #EXTINF 格式如下：
    ```javascript
    #EXTINF:<duration>,<title>
    ```

#### 参数说明：

*   **duration：** 播放的持续时间（以秒为单位）。对于直播流，使用 -1 表示未指定时长或无限时长。
*   **title：** 显示在播放器中的媒体名称。

    示例：
    ```javascript
    #EXTINF:-1, CCTV 1 
    http://example.com/live/cctv1
    ```

*   URL 或媒体文件路径
紧跟在 #EXTINF 行之后的是媒体的实际地址。该地址可以是：

    *   **HTTP 或 HTTPS URL：** 例如 http://example.com/live/stream1
    *   **RTSP 地址：** 例如 rtsp://example.com/stream
    *   **本地文件路径：** 例如 /media/videos/movie.mp4



### 扩展参数
除了基本信息，#EXTINF 行还支持多个扩展属性，用于 IPTV 服务或高级播放器的自定义设置。

*   常见的扩展参数
    *   **tvg-id：** 频道 ID，通常用于匹配电子节目指南（EPG）中的频道。
    ```javascript
    #EXTINF:-1 tvg-id="CCTV-1", CCTV1 
    http://example.com/live/cctv1
    ```

    *   **tvg-name：** 频道名称，与 EPG 系统匹配节目名称。

    ```javascript
    #EXTINF:-1 tvg-name="CCTV 1", CCTV1 
    http://example.com/live/cctv1
    ```

    *   **tvg-logo：** 频道的图标 URL，播放器中显示的频道徽标。

    ```javascript
    #EXTINF:-1 tvg-logo="http://example.com/logo_cctv1.png", CCTV1
    http://example.com/live/cctv1
    ```

    *   **tvg-shift：** EPG 时区偏移量（以小时为单位），适用于回看或跨时区播放。
    ```javascript
    #EXTINF:-1 tvg-shift="2", CCTV1
    http://example.com/live/cctv1
    ```

    *   **group-title：** 将频道分类到特定组，以便播放器对频道进行分组显示。
    ```javascript
    #EXTINF:-1 group-title="新闻", CCTV1 
    http://example.com/live/cctv1
    ```

**示例综合用法**
以下是一个完整的示例，包含了所有常见扩展标签：
```javascript
#EXTM3U 

#EXTINF:-1 tvg-id="CCTV1" tvg-name="CCTV1" tvg-logo="http://xx.com/logo_cctv1.png" group-title="央视" tvg-shift="0", CCTV1
http://example.com/live/cctv1
```

### M3U 文件的实际应用场景
*    **IPTV 直播：** IPTV 播放列表用于组织直播频道，并为播放器提供流媒体源。
*    **回看功能：** 通过带有时间戳的 URL 支持回放过去的节目（如示例中的 start 和 end 参数）。
*    **节目指南匹配：** 使用 tvg-id、tvg-name 和 tvg-shift 等参数，确保播放频道与 EPG 节目表一致。

#### 注意事项
*    **播放器兼容性：** 不同播放器可能支持不同的扩展参数，因此在实际应用中应测试播放器的兼容性。

*    **参数顺序：** 在 #EXTINF 行中，参数可以按任意顺序排列，但习惯上将 tvg-id、tvg-name、tvg-logo 放在前面，group-title 和 tvg-shift 放在最后。



### 总结
M3U 文件格式的灵活性使其能够适应不同的媒体播放需求，尤其是 IPTV 应用。通过正确使用 #EXTINF 和扩展标签，可以为用户提供详细的频道信息、EPG 支持以及回看功能。

## 获取更多，欢迎关注公众号：百宝箱箱
<img src="../assets/GongZhongHao.png" style="max-width:100%; height:auto;">

[返回](..)
