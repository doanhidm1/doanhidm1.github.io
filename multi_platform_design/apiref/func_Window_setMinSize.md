# Window.setMinSize

機能/意味
:   [Windows\*]ウィンドウの最小サイズの設定

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   setMinSize(width, height)

引数
:   |  |  |
    | --- | --- |
    | width | ウィンドウの最小の横幅を指定します。  0を指定すると制限は無くなります。 |
    | height | ウィンドウの最小の縦幅を指定します。  0を指定すると制限は無くなります。 |

戻り値
:   なし (void)

説明
:   ウィンドウの最小サイズを指定します。
    ウィンドウはこのメソッドで指定したサイズより小さくなることはできません。

参照
:   [Window.setMaxSize](func_Window_setMaxSize)
    [Window.setSize](func_Window_setSize)
    [Window.minWidth](prop_Window_minWidth)
    [Window.minHeight](prop_Window_minHeight)