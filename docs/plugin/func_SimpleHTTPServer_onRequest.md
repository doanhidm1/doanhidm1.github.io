# SimpleHTTPServer.onRequest

機能/意味
:   リクエスト処理（イベント）

タイプ
:   [SimpleHTTPServerクラス](class_SimpleHTTPServer)のメソッド

構文
:   onRequest()

引数
:   |  |  |
    | --- | --- |
    | request | = %[ method: メソッドの種類（GET/POST/...） path: リクエストパス request: 生リクエスト（%xx未デコード，?以降も含む） header: %[ リクエストヘッダ（ブラウザの情報等） ] form: %[ フォームデータ ] ]; |

戻り値
:   response = %[\nstatus:ステータスコード（省略可能，エラーが無ければ自動で200）\ncontent\_type: Content-Type名\nerror\_type:エラーの種類（text/file/binaryが無い場合に有効）\nerror\_desc:エラーの説明（text/file/binaryが無い場合に有効）\nredirect: リダイレクトする場合のURI（省略可能）\n\n以下は排他（どれかひとつ，上から優先）\ntext:返すテキスト（codepageで自動エンコードされる）\nfile:返すファイル\nbinary:返すバイナリ（ArrayまたはOctet）\n];

説明