# Window.HWND

機能/意味
:   ウィンドウハンドル

タイプ
:   [Windowクラス](f_Window)のプロパティ (読み出し専用)

説明
:   ウィンドウハンドルを表します。
    　ここで得られるのは整数ですが、プラグインなどでこの数値を使う場合は HWND 型に
    キャストして使ってください。
    　[Window.borderStyle](f_Window_borderStyle) など、一部のプロパティは値が変更されるときに
    ウィンドウをいったん破棄し、作り替えますので注意してください。

参照
:   [Window.registerMessageReceiver](f_Window_registerMessageReceiver)