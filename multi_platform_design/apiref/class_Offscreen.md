# Offscreen

オフスクリーン。
いわゆるレンダーターゲット。テクスチャとしても利用可能です。
内部的に FBO, Renderbuffer, Texture が生成されます。
レンダーターゲットとして設定しないのであれば、わざわざこのクラスを使用する必要性はありません。
Textureクラスを使用した方がメモリ効率が良いです。

# メンバ

コンストラクタ
:   [Offscreen](func_Offscreen_Offscreen) (オフスクリーンを生成。 )

メソッド
:   [copyRect](func_Offscreen_copyRect) (矩形コピー )
    [copyRect](func_Offscreen_copyRect_1) (矩形コピー )
    [copyTo](func_Offscreen_copyTo) (Bitmapにコピー )
    [copyTo](func_Offscreen_copyTo_1) (Bitmapにコピー )
    [copyTo](func_Offscreen_copyTo_2) (Bitmapにコピー )
    [exchangeTexture](func_Offscreen_exchangeTexture) (フレームバッファに設定されているテクスチャとTextureクラスが指すテクスチャを入れ替える。 )

プロパティ
:   [height](prop_Offscreen_height) (高さ、生成時に指定されたもの[r] )
    [nativeHandle](prop_Offscreen_nativeHandle) (環境依存のハンドル[r] )
    [width](prop_Offscreen_width) (幅、生成時に指定されたもの[r] )

イベント