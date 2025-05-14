# Canvas.drawTexture

機能/意味
:   1枚のテクスチャを描画

タイプ
:   [Canvasクラス](class_Canvas)のメソッド

構文
:   drawTexture(texture:Texture)

引数
:   |  |  |
    | --- | --- |
    | texture | 描画に使用するテクスチャを指定します |

戻り値
:   なし (void)

説明
:   defaultShaderで描画されます。
    位置や拡大縮小、回転は matrix で指定します。
    テクスチャはTextureクラスだけでなく、Offscreenクラスを指定しても問題ありません。
    Offscreenクラスを指定する場合は、renderTargetからそのOffscreenクラスは外されていることが前提(循環しないように)です。