# Layer.getLayerAt

機能/意味
:   指定位置のレイヤを取得

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   getLayerAt(x, y, exclude\_self=false, get\_disabled=false)

引数
:   |  |  |
    | --- | --- |
    | x | 取得したいレイヤの位置の x 座標を表示座標上でピクセル単位で指定します。  このメソッドを実行するレイヤの表示座標が用いられます ( プライマリレイヤ上の表示座標ではありません ) |
    | y | 取得したいレイヤの位置の y 座標を表示座標上でピクセル単位で指定します。  このメソッドを実行するレイヤの表示座標が用いられます ( プライマリレイヤ上の表示座標ではありません ) |
    | exclude\_self | レイヤの検索から自分自身を除外するかどうかを指定します。  偽を指定すると、自分自身のレイヤも検索に含まれます。  真を指定すると、自分自身のレイヤは検索から除外され、あたかも存在しないかのように扱われます。  この引数を省略すると偽が指定されたと見なされます。 |
    | get\_disabled | 無効になっているレイヤのオブジェクトを得るかどうかを指定します。  偽を指定すると、無効 (Layer.enabled プロパティが偽など) になっているレイヤが指定位置にあった場合、null が返ります。  真を指定すると、無効になっているレイヤが指定位置にあった場合は、そのレイヤオブジェクトを返します。  この引数を省略すると偽が指定されたと見なされます。 |

戻り値
:   指定位置にあったレイヤオブジェクト。
    指定位置にレイヤが無かった場合などは null が戻ります。

説明
:   x,y で示された位置にあるレイヤオブジェクトを返します。
    当たり判定は通常のマウスイベントの当たり判定と同じ機構が用いられます。
    つまり、指定位置を、レイヤの重ね順において一番手前から見ていき、最初に当たり判定に該当したレイヤが返されます。
    exclude\_self 引数で真を指定すると、このメソッドを実行するレイヤを検索の対象から除外することができます。

参照
:   [Layer.hitType](prop_Layer_hitType)
    [Layer.hitThreshold](prop_Layer_hitThreshold)
    [Layer.onHitTest](event_Layer_onHitTest)