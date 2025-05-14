# Canvas.drawTexture

機能/意味
:   3枚のテクスチャをシェーダー指定して描画

タイプ
:   [Canvasクラス](class_Canvas)のメソッド

構文
:   drawTexture(texture:Texture, texture2:Texture, texture3:Texture, shader:ShaderProgram)

引数
:   |  |  |
    | --- | --- |
    | texture | 描画に使用するテクスチャを指定します |
    | texture2 | 描画に使用する2枚目のテクスチャを指定します |
    | texture3 | 描画に使用する3枚目のテクスチャを指定します |
    | shader | 描画に使用するシェーダーを指定します |

戻り値
:   なし (void)

説明
:   OpenGL ES 2.0の場合はテクスチャ最大8枚、3.0は頂点側最大16枚，フラグメント側最大16枚なので、まだ追加できますが、とりあえずは3枚まで定義しています。
    将来的にはテクスチャを配列で渡すバージョンを作り、4枚以上はそちらで対応も検討します。