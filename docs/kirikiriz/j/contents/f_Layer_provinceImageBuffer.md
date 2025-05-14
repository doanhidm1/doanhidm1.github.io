# Layer.provinceImageBuffer

機能/意味
:   領域画像バッファポインタ

タイプ
:   [Layerクラス](f_Layer)のプロパティ (読み出し専用)

説明
:   領域画像 ( 領域の情報を含む 8bpp のビットマップ ) の画像バッファ左上隅へのポインタ
    を表します。
    　このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供する
    ためにあります。
    　整数型で返されますが、プラグインなどでは適切な型 ( const unsigned char \* 等 ) にキャストして使って
    ください。
    　このプロパティで得られたポインタには値を書き込まないでください。
    [Layer.provinceImageBufferForWrite](f_Layer_provinceImageBufferForWrite) で得られたポインタならば書き込むことができます。
    　画像が割り当てられていない場合は NULL (0) が返ります。画像が割り当てられていない場合は
    全域が領域番号 0 であると見なす必要があります。
    　画像のサイズは [Layer.imageWidth](f_Layer_imageWidth) と [Layer.imageHeight](f_Layer_imageHeight) プロパティが
    表しています。
    　ポインタの計算方法は [Layer.provinceImageBufferPitch](f_Layer_provinceImageBufferPitch) を参照してください。

参照
:   [Layer.provinceImageBufferForWrite](f_Layer_provinceImageBufferForWrite)
    [Layer.provinceImageBufferPitch](f_Layer_provinceImageBufferPitch)