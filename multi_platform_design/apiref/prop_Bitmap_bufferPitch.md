# Bitmap.bufferPitch

機能/意味
:   画像バッファピッチ

タイプ
:   [Bitmapクラス](class_Bitmap)のプロパティ

説明
:   画像 ( 色とマスク(不透明度)の情報を含む 32bpp のビットマップ ) の画像バッファのピッチ( 一つ下のスキャンラインまでのバイト数 ) を表します。
    このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供するためにあります。
    tjs*uint32 が 32bit の整数型、tjs*uint8 が 8bit (1byte) の整数型として、画像位置 (x, y) へのポインタは C 言語で書くと以下のように計算することができます。
    ( (tjs*uint32\*)( (tjs*uint8*)buffer + y*bufferPitch )) + x
    このプロパティは、次のスキャンラインまでのピクセル数ではなく、バイト数を返すことに注意してください。
    この数値は画像横幅ぴったりに必要なバイト数よりも若干大きい場合があります。
    このプロパティは値が負になり得ますので注意してください。

参照
:   [Bitmap.buffer](prop_Bitmap_buffer)
    [Bitmap.bufferForWrite](prop_Bitmap_bufferForWrite)