# VideoOverlay.onCallbackCommand

機能/意味
:   コールバックコマンドが発生した

タイプ
:   [VideoOverlayクラス](f_VideoOverlay)のイベント

構文
:   onCallbackCommand(command, arg)

引数
:   |  |  |
    | --- | --- |
    | command | コマンド名を表す文字列です。 |
    | arg | コマンドに対する引数を表す文字列です。 |

説明
:   SWF 再生中に、Get URL アクション (指定 URL を開くアクション) が実行されたときに発生します。
    SWF コンテンツ上で、このアクションの URL として 「FSCommand:(コマンド名)」 を指定し、
    ターゲットウィンドウに引数を指定するとこのイベントを発生させることができます。