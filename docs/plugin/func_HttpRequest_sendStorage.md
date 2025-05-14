# HttpRequest.sendStorage

機能/意味
:   リクエストの送信。送受信は非同期実行されます。

タイプ
:   [HttpRequestクラス](class_HttpRequest)のメソッド

構文
:   sendStorage(storage, storeStorage)

引数
:   |  |  |
    | --- | --- |
    | storage | 送信するファイルデータ |
    | storeStrorage | レスポンス保存先ファイル。指定された場合はプロパティ responseは 設定されません |

戻り値
:   なし (void)

説明
:   エラー時も例外は発生しませんので、readyState と status で判定してください。