# Bitmap

Bitmap クラスは、画像情報を保持するクラスです。

# メンバ

コンストラクタ
:   [Bitmap](func_Bitmap_Bitmap) (デフォルトBitmapオブジェクトの構築 )
    [Bitmap](func_Bitmap_Bitmap_1) (大きさを指定したBitmapオブジェクトの構築 )
    [Bitmap](func_Bitmap_Bitmap_2) (ファイルを指定したBitmapオブジェクトの構築 )

メソッド
:   [copyFrom](func_Bitmap_copyFrom) (画像のコピー )
    [getMaskPixel](func_Bitmap_getMaskPixel) (ピクセルのアルファ値の取得 )
    [getPixel](func_Bitmap_getPixel) (ピクセル値の取得 )
    [getSaveOption](func_Bitmap_getSaveOption) (画像保存追加情報取得(1.3.0以降) )
    [independ](func_Bitmap_independ) (画像の共有の解除 )
    [load](func_Bitmap_load) (画像の読み込み )
    [loadAsync](func_Bitmap_loadAsync) (画像の非同期読み込み )
    [loadHeader](func_Bitmap_loadHeader) (画像情報の読み込み(1.3.0以降) )
    [save](func_Bitmap_save) (画像の保存 )
    [setMaskPixel](func_Bitmap_setMaskPixel) (ピクセルのアルファ値の取得 )
    [setPixel](func_Bitmap_setPixel) (ピクセル値の設定 )
    [setSize](func_Bitmap_setSize) (画像サイズの設定 )

プロパティ
:   [buffer](prop_Bitmap_buffer) (画像バッファポインタ )
    [bufferForWrite](prop_Bitmap_bufferForWrite) (画像バッファポインタ(書き込み用) )
    [bufferPitch](prop_Bitmap_bufferPitch) (画像バッファピッチ )
    [height](prop_Bitmap_height) (画像縦幅 )
    [loading](prop_Bitmap_loading) (非同期読込み中確認 )
    [width](prop_Bitmap_width) (画像横幅 )

イベント
:   [onLoaded](event_Bitmap_onLoaded) (非同期読込みが完了した )