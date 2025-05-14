# HttpRequest.send

機能/意味
:   リクエストの送信。送信処理は非同期実行されます。

タイプ
:   [HttpRequestクラス](class_HttpRequest)のメソッド

構文
:   send(data, storeStorage)

引数
:   |  |  |
    | --- | --- |
    | data | 送信するデータ octetの場合 : そのまま送信 文字列の場合 : 規定のエンコードで処理して送信 その他 : データは送信されません |
    | storeStrorage | レスポンス保存先ファイル。指定された場合はプロパティ responseは 設定されません |

戻り値
:   なし (void)

説明
:   エラー時も例外は発生しませんので、readyState と status で判定してください。