# Layer.mainImageBufferForWrite

機能/意味
:   メイン画像バッファポインタ(書き込み用)

タイプ
:   [Layerクラス](class_Layer)のプロパティ

説明
:   メイン画像 ( 色とマスク(不透明度)の情報を含む 32bpp のビットマップ ) の画像バッファ左上隅へのポインタを表します。
    このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供するためにあります。
    整数型で返されますが、プラグインなどでは適切な型 ( unsigned long \* 等 ) にキャストして使ってください。
    このプロパティで得られたポインタには Layer.mainImageBuffer と異なり、値を書き込むことができます。
    吉里吉里内部では全く同じ画像は複数のレイヤ間等で共有しますが、このプロパティを参照するとその共有状態を解除します。
    レイヤに画像が割り当てられていない場合は NULL (0) が返ります。
    画像のサイズは Layer.imageWidth と Layer.imageHeight プロパティが表しています。
    ポインタの計算方法は Layer.mainImageBufferPitch を参照してください。

参照
:   [Layer.mainImageBuffer](prop_Layer_mainImageBuffer)
    [Layer.mainImageBufferPitch](prop_Layer_mainImageBufferPitch)