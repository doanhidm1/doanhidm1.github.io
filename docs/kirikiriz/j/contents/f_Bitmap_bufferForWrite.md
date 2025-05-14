# Bitmap.bufferForWrite

機能/意味
:   画像バッファポインタ(書き込み用)

タイプ
:   [Bitmapクラス](f_Bitmap)のプロパティ (読み出し専用)

説明
:   画像 ( 色とマスク(不透明度)の情報を含む 32bpp のビットマップ ) の画像バッファ左上隅へのポインタ
    を表します。
    　このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供する
    ためにあります。
    　整数型で返されますが、プラグインなどでは適切な型 ( unsigned long \* 等 ) にキャストして使って
    ください。
    　このプロパティで得られたポインタには [Bitmap.buffer](f_Bitmap_buffer) と異なり、
    値を書き込むことができます。吉里吉里内部では全く同じ画像は複数のオブジェト間で共有しますが、
    このプロパティを参照するとその共有状態を解除します。
    　画像のサイズは [Bitmap.width](f_Bitmap_width) と [Bitmap.height](f_Bitmap_height) プロパティが
    表しています。
    　ポインタの計算方法は [Bitmap.bufferPitch](f_Bitmap_bufferPitch) を参照してください。

参照
:   [Bitmap.buffer](f_Bitmap_buffer)
    [Bitmap.bufferPitch](f_Bitmap_bufferPitch)