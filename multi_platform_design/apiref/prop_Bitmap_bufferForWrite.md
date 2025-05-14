# Bitmap.bufferForWrite

機能/意味
:   画像バッファポインタ(書き込み用)

タイプ
:   [Bitmapクラス](class_Bitmap)のプロパティ

説明
:   画像 ( 色とマスク(不透明度)の情報を含む 32bpp のビットマップ ) の画像バッファ左上隅へのポインタを表します。
    このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供するためにあります。
    整数型で返されますが、プラグインなどでは適切な型 ( unsigned long \* 等 ) にキャストして使ってください。
    このプロパティで得られたポインタには Bitmap.buffer と異なり、値を書き込むことができます。
    吉里吉里内部では全く同じ画像は複数のオブジェト間で共有しますが、このプロパティを参照するとその共有状態を解除します。
    画像のサイズは Bitmap.width と Bitmap.height プロパティが表しています。
    ポインタの計算方法は Bitmap.bufferPitch を参照してください。

参照
:   [Bitmap.buffer](prop_Bitmap_buffer)
    [Bitmap.bufferPitch](prop_Bitmap_bufferPitch)