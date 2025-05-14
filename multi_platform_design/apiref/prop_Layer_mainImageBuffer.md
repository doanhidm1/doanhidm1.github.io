# Layer.mainImageBuffer

機能/意味
:   メイン画像バッファポインタ

タイプ
:   [Layerクラス](class_Layer)のプロパティ

説明
:   メイン画像 ( 色とマスク(不透明度)の情報を含む 32bpp のビットマップ ) の画像バッファ左上隅へのポインタを表します。
    このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供するためにあります。
    整数型で返されますが、プラグインなどでは適切な型 ( const unsigned long \* 等 ) にキャストして使ってください。
    このプロパティで得られたポインタには値を書き込まないでください。
    Layer.mainImageBufferForWrite で得られたポインタならば書き込むことができます。
    レイヤに画像が割り当てられていない場合は NULL (0) が返ります。
    画像のサイズは Layer.imageWidth と Layer.imageHeight プロパティが表しています。
    ポインタの計算方法は Layer.mainImageBufferPitch を参照してください。

参照
:   [Layer.mainImageBufferForWrite](prop_Layer_mainImageBufferForWrite)
    [Layer.mainImageBufferPitch](prop_Layer_mainImageBufferPitch)