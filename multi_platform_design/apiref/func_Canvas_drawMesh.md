# Canvas.drawMesh

機能/意味
:   メッシュ描画のインデックスバッファ使用版

タイプ
:   [Canvasクラス](class_Canvas)のメソッド

構文
:   drawMesh(shader:ShaderProgram, index:VertexBinder, count:int, primitiveType:int=VertexBuffer.ptTriangles)

引数
:   |  |  |
    | --- | --- |
    | shader | テクスチャや頂点情報まで関連付けられたシェーダーを指定する |
    | index | インデックスバッファを指定する |
    | count | 描画するインデックス数 |
    | primitiveType | トライアングルなどの指定 |

戻り値
:   なし (void)

説明
:   メッシュ(VertexBinder:頂点情報)は、呼び出し前にshaderに関連付け(プロパティで設定)しておく必要があります。
    テクスチャ情報も同様に関連付けしておく必要があります。
    呼出し後shaderに関連付けた情報は解除(=void)してください。