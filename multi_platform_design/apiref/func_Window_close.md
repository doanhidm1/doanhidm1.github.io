# Window.close

機能/意味
:   ウィンドウを閉じる

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   close()

引数

戻り値
:   なし (void)

説明
:   Window.showModal メソッドで表示されたウィンドウを閉じます。
    ウィンドウを閉じる前に Window.onCloseQuery イベントが発生し、ウィンドウを閉じることができるかどうかを確認することができます。
    Androidでは Window.onCloseQuery イベントは発生せず、Activity.finish() がコールされて終了します。

参照
:   [Window.showModal](func_Window_showModal)
    [Window.onCloseQuery](event_Window_onCloseQuery)