# Window.setMaxSize

機能/意味
:   [Windows\*]ウィンドウの最大サイズの設定

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   setMaxSize(width, height)

引数
:   |  |  |
    | --- | --- |
    | width | ウィンドウの最大の横幅を指定します。  0を指定すると制限は無くなります。 |
    | height | ウィンドウの最大の縦幅を指定します。  0を指定すると制限は無くなります。 |

戻り値
:   なし (void)

説明
:   ウィンドウの最大サイズを指定します。
    ウィンドウはこのメソッドで指定したサイズより大きくなることはできません。

参照
:   Window.setMixSize
    [Window.setSize](func_Window_setSize)
    [Window.maxWidth](prop_Window_maxWidth)
    [Window.maxHeight](prop_Window_maxHeight)