# Window.onPopupHide

機能/意味
:   ポップアップウィンドウを閉じる

タイプ
:   [Windowクラス](f_Window)のイベント

構文
:   onPopupHide()

引数
:   なし

説明
:   ポップアップウィンドウが閉じるべき時に発生するイベントです。このイベントは、[Window.stayOnTop](f_Window_stayOnTop) プロパティが真で、かつ、[Window.focusable](f_Window_focusable) プロパティが偽の場合、「他のウィンドウがクリックされた」あるいは「他のアプリケーションがアクティブになった」時に発生します。
    　通常は、ここでウィンドウを閉じたり、非表示にする処理を行ってください。

参照
:   [Window.focusable](f_Window_focusable)
    [Window.stayOnTop](f_Window_stayOnTop)