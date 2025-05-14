# Window.onPopupHide

機能/意味
:   [Windows\*]ポップアップウィンドウを閉じる

タイプ
:   [Windowクラス](class_Window)のイベント

構文
:   onPopupHide()

引数

戻り値
:   なし (void)

説明
:   ポップアップウィンドウが閉じるべき時に発生するイベントです。
    このイベントは、Window.stayOnTop プロパティが真で、かつ、Window.focusable プロパティが偽の場合、「他のウィンドウがクリックされた」あるいは「他のアプリケーションがアクティブになった」時に発生します。
    通常は、ここでウィンドウを閉じたり、非表示にする処理を行ってください。

参照
:   [Window.focusable](prop_Window_focusable)
    [Window.stayOnTop](prop_Window_stayOnTop)