# Layer.provinceImageBufferForWrite

機能/意味
:   領域画像バッファポインタ(書き込み用)

タイプ
:   [Layerクラス](f_Layer)のプロパティ (読み出し専用)

説明
:   領域画像 ( 領域の情報を含む 8bpp のビットマップ ) の画像バッファ左上隅へのポインタ
    を表します。
    　このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供する
    ためにあります。
    　整数型で返されますが、プラグインなどでは適切な型 ( unsigned char \* 等 ) にキャストして使って
    ください。
    　このプロパティで得られたポインタには [Layer.provinceImageBuffer](f_Layer_provinceImageBuffer) と異なり、
    値を書き込むことができます。吉里吉里内部では全く同じ画像は複数のレイヤ間等で共有しますが、
    このプロパティを参照するとその共有状態を解除します。
    　レイヤに画像が割り当てられていない場合は自動的にこのプロパティを参照した時点で
    割り当てられ、全域が領域番号 0 で初期化されます。
    　画像のサイズは [Layer.imageWidth](f_Layer_imageWidth) と [Layer.imageHeight](f_Layer_imageHeight) プロパティが
    表しています。
    　ポインタの計算方法は [Layer.provinceImageBufferPitch](f_Layer_provinceImageBufferPitch) を参照してください。

参照
:   [Layer.provinceImageBuffer](f_Layer_provinceImageBuffer)
    [Layer.provinceImageBufferPitch](f_Layer_provinceImageBufferPitch)