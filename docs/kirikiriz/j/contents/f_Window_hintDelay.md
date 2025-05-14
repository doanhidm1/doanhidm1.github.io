# Window.hintDelay

機能/意味
:   ヒント表示待ち時間

タイプ
:   [Windowクラス](f_Window)のプロパティ (読み書き可能)

説明
:   ヒントの表示待ち時間をミリ秒単位で表します。値を設定することもできます。
    　デフォルトは500ミリ秒です。
    　0を設定すると即座に [Window.onHintChanged](f_Window_onHintChanged) が呼び出されます(常時表示状態)。
    　-1を設定するとヒントが表示されることはありません。

参照
:   [Window.onHintChanged](f_Window_onHintChanged)