# Window.hintDelay

機能/意味
:   [Windows\*]ヒント表示待ち時間

タイプ
:   [Windowクラス](class_Window)のプロパティ

説明
:   ヒントの表示待ち時間をミリ秒単位で表します。
    値を設定することもできます。
    デフォルトは500ミリ秒です。
    0を設定すると即座に Window.onHintChanged が呼び出されます(常時表示状態)。
    -1を設定するとヒントが表示されることはありません。

参照
:   [Window.onHintChanged](event_Window_onHintChanged)