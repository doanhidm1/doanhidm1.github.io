# Window.onEnterMenuLoop

機能/意味
:   ■拡張イベント：メニュー処理の開始・終了通知

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   onEnterMenuLoop()

引数

戻り値
:   なし (void)

説明
:   ウィンドウのメニュー処理（クリックやF10を押した場合など）の開始と終了の通知イベント
    WM\_ENTERMENULOOP / WM\_EXITMENULOOP 通知のコールバック

    ※フルスクリーンにした場合のメニューではこのイベントは発生しないので注意！