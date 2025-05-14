# Bitmap

Bitmap クラスは、画像情報を保持するクラスです。

# メンバ

コンストラクタ
:   [Bitmap](f_Bitmap_Bitmap)
    [Bitmap](f_Bitmap_Bitmap_1)
    [Bitmap](f_Bitmap_Bitmap_2)

メソッド
:   [copyFrom](f_Bitmap_copyFrom) ( 画像のコピー )
    [getMaskPixel](f_Bitmap_getMaskPixel) ( ピクセルのアルファ値の取得 )
    [getPixel](f_Bitmap_getPixel) ( ピクセル値の取得 )
    [getSaveOption](f_Bitmap_getSaveOption) ( 画像保存追加情報取得(1.3.0以降) )
    [independ](f_Bitmap_independ) ( 画像の共有の解除 )
    [load](f_Bitmap_load) ( 画像の読み込み )
    [loadAsync](f_Bitmap_loadAsync) ( 画像の非同期読み込み )
    [loadHeader](f_Bitmap_loadHeader) ( 画像情報の読み込み(1.3.0以降) )
    [save](f_Bitmap_save) ( 画像の保存 )
    [setMaskPixel](f_Bitmap_setMaskPixel) ( ピクセルのアルファ値の取得 )
    [setPixel](f_Bitmap_setPixel) ( ピクセル値の設定 )
    [setSize](f_Bitmap_setSize) ( 画像サイズの設定 )

プロパティ
:   [buffer](f_Bitmap_buffer) ( 画像バッファポインタ )
    [bufferForWrite](f_Bitmap_bufferForWrite) ( 画像バッファポインタ(書き込み用) )
    [bufferPitch](f_Bitmap_bufferPitch) ( 画像バッファピッチ )
    [height](f_Bitmap_height) ( 画像縦幅 )
    [loading](f_Bitmap_loading) ( 非同期読込み中確認 )
    [width](f_Bitmap_width) ( 画像横幅 )

イベント
:   [onLoaded](f_Bitmap_onLoaded) ( 非同期読込みが完了した )