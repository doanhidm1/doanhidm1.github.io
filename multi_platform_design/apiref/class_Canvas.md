# Canvas

Canvasは描画機能を提供するクラスです。
Windowを生成すると、プロパティcanvasが自動的に作られます。
使用する時は、このWindowのcanvasプロパティを使用します。

# メンバ

メソッド
:   [capture](func_Canvas_capture) (現在の描画内容全体をBitmap/Texture/Offscreenにキャプチャ )
    [clear](func_Canvas_clear) (描画領域全体をクリア )
    [draw9Patch](func_Canvas_draw9Patch) (9patchを利用して描画 )
    [drawMesh](func_Canvas_drawMesh) (メッシュ描画のインデックスバッファ使用版 )
    [drawMesh](func_Canvas_drawMesh_1) (メッシュ描画 )
    [drawText](func_Canvas_drawText) (テキスト描画(未実装) )
    [drawTexture](func_Canvas_drawTexture) (2枚のテクスチャをシェーダー指定して描画 )
    [drawTexture](func_Canvas_drawTexture_1) (3枚のテクスチャをシェーダー指定して描画 )
    [drawTexture](func_Canvas_drawTexture_2) (1枚のテクスチャを描画 )
    [drawTexture](func_Canvas_drawTexture_3) (1枚のテクスチャをシェーダー指定して描画 )
    [drawTextureAtlas](func_Canvas_drawTextureAtlas) (テクスチャの一部分を描画 )
    [drawTextureAtlas](func_Canvas_drawTextureAtlas_1) (テクスチャの一部分を描画(シェーダー指定あり) )
    [fill](func_Canvas_fill) (色での塗りつぶし )
    [flush](func_Canvas_flush) (描画をフラッシュする )
    [restore](func_Canvas_restore) (matrix と clip の状態を復元する(スタック) )
    [save](func_Canvas_save) (matrix と clip の状態を保存する(スタック) )

プロパティ
:   [blendMode](prop_Canvas_blendMode) (描画の合成モード指定 )
    [clearColor](prop_Canvas_clearColor) (クリア色指定・描画処理前の画面クリア色 )
    [clipRect](prop_Canvas_clipRect) (クリッピング用矩形のRectクラス )
    [defaultFillShader](prop_Canvas_defaultFillShader) (fill時に使用されるデフォルトのシェーダー )
    [defaultShader](prop_Canvas_defaultShader) (テクスチャの描画に使用されるデフォルトのシェーダー(drawTextureでtexture1枚のみ渡した時のシェーダー) )
    [enableClipRect](prop_Canvas_enableClipRect) (矩形でクリッピングするかどうかの設定 )
    [enableCulling](prop_Canvas_enableCulling) (表裏カリングを行うかどうかの設定 )
    [height](prop_Canvas_height) (描画領域の高さ )
    [matrix](prop_Canvas_matrix) (描画マトリックス指定 )
    [renderTarget](prop_Canvas_renderTarget) (描画ターゲット指定 )
    [width](prop_Canvas_width) (描画領域の幅 )

イベント