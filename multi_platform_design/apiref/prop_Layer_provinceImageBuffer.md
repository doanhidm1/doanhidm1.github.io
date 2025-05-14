# Layer.provinceImageBuffer

機能/意味
:   領域画像バッファポインタ

タイプ
:   [Layerクラス](class_Layer)のプロパティ

説明
:   領域画像 ( 領域の情報を含む 8bpp のビットマップ ) の画像バッファ左上隅へのポインタを表します。
    このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供するためにあります。
    整数型で返されますが、プラグインなどでは適切な型 ( const unsigned char \* 等 ) にキャストして使ってください。
    このプロパティで得られたポインタには値を書き込まないでください。
    Layer.provinceImageBufferForWrite で得られたポインタならば書き込むことができます。
    画像が割り当てられていない場合は NULL (0) が返ります。
    画像が割り当てられていない場合は全域が領域番号 0 であると見なす必要があります。
    画像のサイズは Layer.imageWidth と Layer.imageHeight プロパティが表しています。
    ポインタの計算方法は Layer.provinceImageBufferPitch を参照してください。

参照
:   [Layer.provinceImageBufferForWrite](prop_Layer_provinceImageBufferForWrite)
    [Layer.provinceImageBufferPitch](prop_Layer_provinceImageBufferPitch)