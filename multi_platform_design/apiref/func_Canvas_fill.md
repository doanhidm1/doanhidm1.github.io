# Canvas.fill

機能/意味
:   色での塗りつぶし

タイプ
:   [Canvasクラス](class_Canvas)のメソッド

構文
:   fill(width:int, height:int, colors=-1, shader=null)

引数
:   |  |  |
    | --- | --- |
    | width | 塗りつぶし範囲幅 |
    | height | 塗りつぶし範囲高さ |
    | colors | 4頂点の頂点カラーARGB。単独数値なら単色、配列なら4頂点個別指定 |
    | shader | 塗りつぶしシェーダー。nullの時defaultFillShaderで塗りつぶされる |

戻り値
:   なし (void)

説明
:   XY座標はmatrixで指定する。