# Bitmap.buffer

機能/意味
:   画像バッファポインタ

タイプ
:   [Bitmapクラス](class_Bitmap)のプロパティ

説明
:   画像 ( 色とマスク(不透明度)の情報を含む 32bpp のビットマップ ) の画像バッファ左上隅へのポインタを表します。
    このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供するためにあります。
    整数型で返されますが、プラグインなどでは適切な型 ( const unsigned long \* 等 ) にキャストして使ってください。
    このプロパティで得られたポインタには値を書き込まないでください。
    Bitmap.bufferForWrite で得られたポインタならば書き込むことができます。
    画像のサイズは Bitmap.width と Bitmap.height プロパティが表しています。
    ポインタの計算方法は Bitmap.bufferPitch を参照してください。

参照
:   [Bitmap.bufferForWrite](prop_Bitmap_bufferForWrite)
    [Bitmap.bufferPitch](prop_Bitmap_bufferPitch)