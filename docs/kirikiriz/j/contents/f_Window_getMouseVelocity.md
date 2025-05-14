# Window.getMouseVelocity

機能/意味
:   マウス座標移動速度の取得(1.1.0以降)

タイプ
:   [Windowクラス](f_Window)のメソッド

構文
:   getMouseVelocity(x, y, speed)

引数
:   |  |  |
    | --- | --- |
    | x | X軸方向のマウス座標移動速度が返ります。 |
    | y | Y軸方向のマウス座標移動速度が返ります。 |
    | speed | マウス座標移動速度が返ります。 |

戻り値
:   取得が成功したか失敗したかが返ります

説明
:   現在のマウス移動速度を pixel / sec で取得します。
    　ウィンドウ内に入った瞬間から計測開始されています。
    　[Window.resetMouseVelocity](f_Window_resetMouseVelocity) を使用して計測をリセットし、任意のタイミングか計測得できるように出来ます。

参照
:   [Window.getTouchVelocity](f_Window_getTouchVelocity)
    [Window.resetMouseVelocity](f_Window_resetMouseVelocity)