# BinaryStream.setProgressCallback

機能/意味
:   プログレスコールバックを設定する

タイプ
:   [BinaryStreamクラス](class_BinaryStream)のメソッド

構文
:   setProgressCallback(callback)

引数
:   |  |  |
    | --- | --- |
    | callback | コールバック関数 function(storage, read\_size) { return true\_if\_cancel; } voidの場合は解除 |

戻り値
:   なし (void)

説明
:   copy/compress/decompress の処理中からコールバックする関数を設定します。
    コールバックは（現在の実装では） 1MiB 読む毎時および最後まで読んだ時に呼び返されます。
    コールバックから true を返すと処理がキャンセルできます。
    ※コールバックの間隔は変更される場合があります

    TJS的には処理が固まってしまうのは仕様ですが，別途 windowExProgress プラグインなどを
    使用することで，ユーザーからのキャンセルを受け付けられるようになります。