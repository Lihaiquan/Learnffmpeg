## libavcodec 库的结构体
###  结构体 struct AVCodecContext 介绍
#### 1. AVMediaType codec_type   媒体类型
 -  AVMediaType 枚举定义如下
   >>>  ```javascript
     enum AVMediaType {
       AVMEDIA_TYPE_UNKNOWN = -1,  ///< Usually treated as AVMEDIA_TYPE_DATA
       AVMEDIA_TYPE_VIDEO,
       AVMEDIA_TYPE_AUDIO,
       AVMEDIA_TYPE_DATA,          ///< Opaque data information usually continuous
       AVMEDIA_TYPE_SUBTITLE,
       AVMEDIA_TYPE_ATTACHMENT,    ///< Opaque data information usually sparse
       AVMEDIA_TYPE_NB
   };
   >>> ```

   #### 2. const struct AVCodec  *codec; // 解码器
   #### 3. enum AVCodecID     codec_id;  // 解码器对应的id
   - 解码器ID是标识数据流的组织方式（那种压缩规则）如果两个解码器具有相同的ID，则可以对同一个数据流解码； 同理，两个编码器具有相同的 ID，可以编码相互兼容的字节流（规则相同）
   - AVCodecID 枚举定义如下: 

   >>>  ```javascript
      enum AVCodecID {
         AV_CODEC_ID_NONE,

          /* video codecs */
         AV_CODEC_ID_MPEG1VIDEO,
         AV_CODEC_ID_MPEG2VIDEO, ///< preferred ID for MPEG-1/2 video decoding
         AV_CODEC_ID_H261,
         AV_CODEC_ID_H263,
         AV_CODEC_ID_RV10,
         AV_CODEC_ID_RV20,
         AV_CODEC_ID_MJPEG,
         AV_CODEC_ID_MJPEGB,
         AV_CODEC_ID_LJPEG，
         ........
      }
   >>> ```

     4.unsigned int codec_tag; // 编码器的tag值，用于解决编码器bug



   

