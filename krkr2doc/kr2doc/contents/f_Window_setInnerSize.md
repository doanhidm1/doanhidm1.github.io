# Window.setInnerSize

機能/意味
:   クライアントサイズの設定

タイプ
:   [Windowクラス](f_Window)のメソッド

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
    　クライアントのサイズを指定するときには、[Window.innerWidth](f_Window_innerWidth) や
    [Window.innerHeight](f_Window_innerHeight) プロパティを個々に設定するよりも
    このメソッドで一気に指定した方が効率的です。

参照
:   [Window.innerWidth](f_Window_innerWidth)
    [Window.innerHeight](f_Window_innerHeight)