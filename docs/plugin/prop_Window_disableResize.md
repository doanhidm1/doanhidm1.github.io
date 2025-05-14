# Window.disableResize

機能/意味
:   リサイズの抑制

タイプ
:   [Windowクラス](class_Window)のプロパティ

説明
:   setter は registerExEvent() で拡張イベントを登録していないと例外が発生する
    true に設定すると，borderStyle == bsSizeable の場合でも
    ・ウィンドウ淵のサイズ変更カーソルが出なくなりサイズが変更できなくなる
    ・システムメニュー(Alt+Space)のサイズ変更がグレーになり選択できなくなる
    最大化など他の方法でのサイズ変更は有効(onResizeも飛ぶ)