# Layer.mainImageBuffer

機能/意味
:   メイン画像バッファポインタ

タイプ
:   [Layerクラス](f_Layer)のプロパティ (読み出し専用)

説明
:   メイン画像 ( 色とマスク(不透明度)の情報を含む 32bpp のビットマップ ) の画像バッファ左上隅へのポインタ
    を表します。
    　このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供する
    ためにあります。
    　整数型で返されますが、プラグインなどでは適切な型 ( const unsigned long \* 等 ) にキャストして使って
    ください。
    　このプロパティで得られたポインタには値を書き込まないでください。
    [Layer.mainImageBufferForWrite](f_Layer_mainImageBufferForWrite) で得られたポインタならば書き込むことができます。
    　レイヤに画像が割り当てられていない場合は NULL (0) が返ります。
    　画像のサイズは [Layer.imageWidth](f_Layer_imageWidth) と [Layer.imageHeight](f_Layer_imageHeight) プロパティが
    表しています。
    　ポインタの計算方法は [Layer.mainImageBufferPitch](f_Layer_mainImageBufferPitch) を参照してください。

参照
:   [Layer.mainImageBufferForWrite](f_Layer_mainImageBufferForWrite)
    [Layer.mainImageBufferPitch](f_Layer_mainImageBufferPitch)