# System.addContinuousHandler

機能/意味
:   Continuous ハンドラの追加

タイプ
:   [Systemクラス](class_System)のメソッド

構文
:   addContinuousHandler(callback)

引数
:   |  |  |
    | --- | --- |
    | callback | ハンドラとなる関数を指定します。 |

戻り値
:   なし (void)

説明
:   Continuous ハンドラを登録します。
    Continuous ハンドラは、「できる限り頻繁に」呼び出されるイベントハンドラです。
    他にする処理がない場合、吉里吉里は Continuous ハンドラを呼び出し続けます。
    他にイベントなどが起きた場合はそちらが優先されます。
    ただし、コマンドラインオプションの -contfreq で呼び出しの頻度が指定されている場合はそれに従います。