# HttpRequest

HTTP/HTTPS による非同期通信機能を提供します。
ファイルの送受信処理はバックグラウンド実行されます。

# メンバ

コンストラクタ
:   [HttpRequest](func_HttpRequest_HttpRequest)

メソッド
:   [abort](func_HttpRequest_abort) (現在実行中の送受信のキャンセル )
    [getAllResponseHeaders](func_HttpRequest_getAllResponseHeaders) (すべての HTTPヘッダを取得する )
    [getResponseHeader](func_HttpRequest_getResponseHeader) (指定したHTTPヘッダを取得する )
    [getResponseText](func_HttpRequest_getResponseText) (レスポンスをテキストの形で取得 )
    [onProgress](func_HttpRequest_onProgress) (データ送受信イベント )
    [onReadyStateChange](func_HttpRequest_onReadyStateChange) (readyState が変化した場合のイベント )
    [open](func_HttpRequest_open) (指定したメソッドで指定URLにリクエストする )
    [send](func_HttpRequest_send) (リクエストの送信。送信処理は非同期実行されます。 )
    [sendStorage](func_HttpRequest_sendStorage) (リクエストの送信。送受信は非同期実行されます。 )
    [setRequestHeader](func_HttpRequest_setRequestHeader) (送信時に送られるヘッダーを追加する )

プロパティ
:   [contentLength](prop_HttpRequest_contentLength) (レスポンスの Content-Length )
    [contentType](prop_HttpRequest_contentType) (レスポンスの Content-Type (エンコーディング指定は含まない) )
    [contentTypeEncoding](prop_HttpRequest_contentTypeEncoding) (レスポンスの Content-Type のエンコード指定 )
    [readyState](prop_HttpRequest_readyState) (通信状態。読み込み専用 )
    [response](prop_HttpRequest_response) (レスポンス。読み込み専用。 )
    [responseData](prop_HttpRequest_responseData) (レスポンス｡読み込み専用 )
    [status](prop_HttpRequest_status) (レスポンスの HTTPステータスコード。読み込み専用 )
    [statusText](prop_HttpRequest_statusText) (レスポンスの HTTPステータスの文字列 )

定数
:   LOADED (readyState 読み込み完了 )
    OPEN (readyState 処理開始 )
    RECEIVING (readyState 受信中 )
    SENT (readyState リクエスト送信 )
    UNINITIALIZED (readyState 初期状態 )