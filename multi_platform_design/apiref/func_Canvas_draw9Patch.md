# Canvas.draw9Patch

機能/意味
:   9patchを利用して描画

タイプ
:   [Canvasクラス](class_Canvas)のメソッド

構文
:   draw9Patch(txture:Texture, width:int, height:int, shader:ShaderProgram=null) :Rect

引数
:   |  |  |
    | --- | --- |
    | texture | 描画するテクスチャ |
    | width | 描画する幅 |
    | height | 描画する高さ |
    | shader | 描画に使用するシェーダー。省略可能。 |

戻り値
:   マージン情報を返します。

説明
:   描画に使用するTextureは9patch情報が読み込まれている必要があります。
    指定できるのはTextureクラスのみです。