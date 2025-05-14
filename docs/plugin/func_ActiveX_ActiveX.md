# ActiveX.ActiveX

機能/意味
:   コンストラクタ

タイプ
:   [ActiveXクラス](class_ActiveX)のメソッド

構文
:   ActiveX(name, win, left, top, width, height)

引数
:   |  |  |
    | --- | --- |
    | progIdOrCLSID | 識別名 または CLSIDを文字列で指定 |
    | name | 識別名またはCLSID を文字列で指定。※WIN32OLE の指定とは CLSID の書式が違うので注意 CAxWindow::CreateControl の書式 |
    | win | 指定するとそのウインドウの上に生成します。省略すると独立ウインドウになります。 |
    | left | 表示座標 ウインドウ指定かつ省略の場合はウインドウのクライアント領域の左上 |
    | top | 表示座標 ウインドウ指定かつ省略の場合はウインドウのクライアント領域の左上 |
    | width | 表示サイズ ウインドウ指定かつ省略の場合は親ウインドウのクライアント領域のサイズ |
    | height | 表示サイズ ウインドウ指定かつ省略の場合は親ウインドウのクライアント領域のサイズ |

戻り値
:   なし (void)

説明