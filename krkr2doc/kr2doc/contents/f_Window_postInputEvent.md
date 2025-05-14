# Window.postInputEvent

機能/意味
:   入力イベントの生成

タイプ
:   [Windowクラス](f_Window)のメソッド

構文
:   postInputEvent(eventname, params=null)

引数
:   |  |  |
    | --- | --- |
    | eventname | イベント名称を指定します。以下の文字列で指定します。   * "onKeyDown" は [Window.onKeyDown](f_Window_onKeyDown) イベントを生成します。 * "onKeyPress" は [Window.onKeyPress](f_Window_onKeyPress) イベントを生成します。 * "onKeyUp" は [Window.onKeyUp](f_Window_onKeyUp) イベントを生成します。onKeyDownとonKeyUpは対になるので、onKeyDownを生成したら対応するonKeyUpも生成することを推奨します。 |
    | params | イベントのパラメータが格納された辞書配列を指定します。   * "onKeyDown" イベントや "onKeyUp" イベントでは、"key" に仮想キーコード、"shift" にシフト状態を格納します。"shift" を省略すると 0 であると見なされます。 * "onKeyPress" イベントでは "key" に文字を指定します。 |

戻り値
:   なし (void)

説明
:   入力イベントを生成します。現バージョンではキー入力に関する３つのイベントを生成できます。
    　このメソッドは、イベントを非同期イベントとして生成します。つまり、このメソッドは、対応するイベントハンドラの終了を待たずに帰ります。実際にイベントハンドラが呼ばれて処理が行われるのは、いったん吉里吉里に制御が戻った後となります。
    　入力イベントは、Windowクラスのほか、通常の入力イベントと同じく、Layerクラスの該当するイベントとしても発生します。
    `例:
    postInputEvent('onKeyDown', %[key: VK_UP, shift: ssShift]);
    postInputEvent('onKeyUp',   %[key: VK_UP, shift: ssShift]);
        // 左カーソルキーを押す`