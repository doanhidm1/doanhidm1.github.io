# Window.mouseCursorState

機能/意味
:   マウスカーソル表示状態

タイプ
:   [Windowクラス](f_Window)のプロパティ (読み書き可能)

説明
:   マウスカーソルの表示状態を表します。値を設定することもできます。
    　mcsVisibleを指定すると、マウスカーソルは表示状態になります。これはデフォルトの状態です。
    　mcsTempHiddenを指定すると、マウスカーソルは非表示状態になりますが、少しでもマウスを動かすとmcsVisibleに変わり、表示状態になります。[Window.hideMouseCursor](f_Window_hideMouseCursor)メソッドを呼び出すとこの状態になります。
    　mcsHiddenを指定すると、マウスカーソルは非表示状態になります。マウスを動かしても表示状態にはなりません。