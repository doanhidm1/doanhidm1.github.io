# Bitmap.buffer

機能/意味
:   画像バッファポインタ

タイプ
:   [Bitmapクラス](f_Bitmap)のプロパティ (読み出し専用)

説明
:   画像 ( 色とマスク(不透明度)の情報を含む 32bpp のビットマップ ) の画像バッファ左上隅へのポインタ
    を表します。
    　このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供する
    ためにあります。
    　整数型で返されますが、プラグインなどでは適切な型 ( const unsigned long \* 等 ) にキャストして使って
    ください。
    　このプロパティで得られたポインタには値を書き込まないでください。
    [Bitmap.bufferForWrite](f_Bitmap_bufferForWrite) で得られたポインタならば書き込むことができます。
    　画像のサイズは [Bitmap.width](f_Bitmap_width) と [Bitmap.height](f_Bitmap_height) プロパティが
    表しています。
    　ポインタの計算方法は [Bitmap.bufferPitch](f_Bitmap_bufferPitch) を参照してください。

参照
:   [Bitmap.bufferForWrite](f_Bitmap_bufferForWrite)
    [Bitmap.bufferPitch](f_Bitmap_bufferPitch)