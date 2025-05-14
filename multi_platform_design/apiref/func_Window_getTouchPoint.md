# Window.getTouchPoint

機能/意味
:   タッチ座標の取得

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   getTouchPoint(index)

引数
:   |  |  |
    | --- | --- |
    | index | タッチ座標配列のインデックスを指定します。 |

戻り値
:   なし (void)

説明
:   現在のタッチ座標配列から指定インデックスの座標情報を取得します。
    座標数は Window.touchPointCount プロパティで取得できます。
    座標情報は以下の要素を含む辞書で返されます。

    * startX : このタッチの開始座標の x 座標値 ( クライアント座標系 ) です
    * startY : このタッチの開始座標の y 座標値 ( クライアント座標系 ) です
    * x : このタッチの現在座標の x 座標値 ( クライアント座標系 ) です
    * y : このタッチの現在座標の y 座標値 ( クライアント座標系 ) です
    * ID : このタッチの識別用 IDです

参照
:   [Window.touchPointCount](prop_Window_touchPointCount)