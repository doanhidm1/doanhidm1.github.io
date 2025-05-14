# Window.beginMove

機能/意味
:   ウィンドウ移動の開始

タイプ
:   [Windowクラス](f_Window)のメソッド

構文
:   beginMove()

引数
:   なし

戻り値
:   なし (void)

説明
:   ウィンドウのマウスでの移動を開始します。通常、ウィンドウのタイトルバーをドラッグすると
    ウィンドウを移動することができますが、このメソッドはその動作をシミュレートします。
    　[Window.onMouseDown](f_Window_onMouseDown) イベントハンドラ内でこのメソッドを呼ぶと、任意の箇所で
    ウィンドウをドラッグして移動可能にすることができます。

参照
:   [Window.onMouseDown](f_Window_onMouseDown)