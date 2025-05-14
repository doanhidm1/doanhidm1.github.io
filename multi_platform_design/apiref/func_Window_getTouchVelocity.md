# Window.getTouchVelocity

機能/意味
:   タッチ座標移動速度の取得

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   getTouchVelocity(id, x, y, speed)

引数
:   |  |  |
    | --- | --- |
    | id | タッチIDを指定します。 |
    | x | X軸方向のマウス座標移動速度が返ります。 |
    | y | Y軸方向のマウス座標移動速度が返ります。 |
    | speed | マウス座標移動速度が返ります。 |

戻り値
:   取得が成功したか失敗したかが返ります

説明
:   現在のタッチ移動速度を pixel / sec で取得します。
    押下されてから離されるまでの間計測されています。
    マルチタッチ対応のため ID ごとに速度計測されています。
    Window.onTouchUp イベントのメソッド呼び出しが終了すると計測している速度情報は消えてしまうので注意が必要です。

参照
:   [Window.getMouseVelocity](func_Window_getMouseVelocity)