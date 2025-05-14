# Window.setPos

機能/意味
:   [Windows\*]ウィンドウ位置の設定

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   setPos(left, top)

引数
:   |  |  |
    | --- | --- |
    | left | ウィンドウの左端位置を指定します。 |
    | top | ウィンドウの上端位置を指定します。 |

戻り値
:   なし (void)

説明
:   ウィンドウの位置を指定します。
    ウィンドウの位置を指定するときには、Window.left や Window.top プロパティを個々に設定するよりも このメソッドで一気に指定した方が効率的です。

参照
:   [Window.left](prop_Window_left)
    [Window.top](prop_Window_top)
    [Window.setSize](func_Window_setSize)