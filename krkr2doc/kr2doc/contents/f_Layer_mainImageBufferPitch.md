# Layer.mainImageBufferPitch

機能/意味
:   メイン画像バッファピッチ

タイプ
:   [Layerクラス](f_Layer)のプロパティ (読み出し専用)

説明
:   メイン画像 ( 色とマスク(不透明度)の情報を含む 32bpp のビットマップ ) の画像バッファのピッチ
    ( 一つ下のスキャンラインまでのバイト数 ) を表します。
    　このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供する
    ためにあります。
    　tjs\_uint32 が 32bit の整数型、tjs\_uint8 が 8bit (1byte) の整数型として、画像位置 (x, y) への
    ポインタは C 言語で書くと以下のように計算することができます。
    ( (tjs\_uint32\*)( (tjs\_uint8\*)mainImageBuffer + y\*mainImageBufferPitch )) + x
    　このプロパティは、次のスキャンラインまでのピクセル数ではなく、バイト数を返すことに
    注意してください。この数値は画像横幅ぴったりに必要なバイト数よりも若干大きい場合があります。
    　このプロパティは値が負になり得ますので注意してください。

参照
:   [Layer.mainImageBuffer](f_Layer_mainImageBuffer)
    [Layer.mainImageBufferForWrite](f_Layer_mainImageBufferForWrite)