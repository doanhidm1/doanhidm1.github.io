# Pad.registerExEvent

機能/意味
:   拡張イベントを有効にする（登録失敗で例外が発生）

タイプ
:   [Padクラス](class_Pad)のメソッド

構文
:   registerExEvent()

引数

戻り値
:   なし (void)

説明
:   拡張イベントとして以下が発生：
    onClose 閉じるボタンが押された

    ※borderStyleなどの変更によりウィンドウが作り直されるとイベントが発生しなくなるので注意
    ⇒その場合は再度registerExEvent()を呼ぶ