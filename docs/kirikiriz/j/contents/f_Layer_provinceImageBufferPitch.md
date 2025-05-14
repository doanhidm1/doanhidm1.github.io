# Layer.provinceImageBufferPitch

機能/意味
:   領域画像バッファピッチ

タイプ
:   [Layerクラス](f_Layer)のプロパティ (読み出し専用)

説明
:   領域画像 ( 領域の情報を含む 8bpp のビットマップ ) の画像バッファのピッチ
    ( 一つ下のスキャンラインまでのバイト数 ) を表します。
    　このプロパティは、プラグインなどのために画像バッファへの直接のアクセスの手段を提供する
    ためにあります。
    　tjs\_uint8 が 8bit (1byte) の整数型として、画像位置 (x, y) への
    ポインタは C 言語で書くと以下のように計算することができます。
    (tjs\_uint8\*)provinceImageBuffer + y\*provinceImageBufferPitch + x
    　このプロパティの数値は画像横幅ぴったりに必要なバイト数よりも若干大きい場合があります。
    　このプロパティは値が負になり得ますので注意してください。

参照
:   [Layer.provinceImageBuffer](f_Layer_provinceImageBuffer)
    [Layer.provinceImageBufferForWrite](f_Layer_provinceImageBufferForWrite)