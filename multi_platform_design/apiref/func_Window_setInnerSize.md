# Window.setInnerSize

機能/意味
:   [Windows\*]クライアントサイズの設定

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   setInnerSize(width, height)

引数
:   |  |  |
    | --- | --- |
    | width | クライアントの横幅を指定します。 |
    | height | クライアントの縦幅を指定します。 |

戻り値
:   なし (void)

説明
:   ウィンドウのクライアントサイズを指定します。
    クライアントは、レイヤを表示可能なウィンドウ内の領域です。
    このサイズを設定するとウィンドウのサイズもそれに応じて変化します。
    クライアントのサイズを指定するときには、Window.innerWidth や Window.innerHeight プロパティを個々に設定するよりも このメソッドで一気に指定した方が効率的です。

参照
:   [Window.innerWidth](prop_Window_innerWidth)
    [Window.innerHeight](prop_Window_innerHeight)