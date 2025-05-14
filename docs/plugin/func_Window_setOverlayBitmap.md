# Window.setOverlayBitmap

機能/意味
:   オーバーレイビットマップを表示・消去する

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   setOverlayBitmap(layer)

引数
:   |  |  |
    | --- | --- |
    | layer | ビットマップ画像にコピーするレイヤ（void or省略時はオーバーレイ消去） |

戻り値
:   なし (void)

説明
:   指定画像でクライアント領域に子ウィンドウ（吉里吉里のではなくWindowsのそれ）をかぶせる
    ・拡張イベントが有効でないと例外が発生する
    ・オーバーレイ表示中は吉里吉里のレイヤ側にマウス系のメッセージが一切行かない
    ・実質的に System.eventDisabled=true の時専用
    ・TVP\_WM\_DETACH で自動消去される