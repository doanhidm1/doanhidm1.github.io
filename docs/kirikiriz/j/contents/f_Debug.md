# Debug

Debug クラスは 吉里吉里のデバッグに関する機能を提供するクラスです。このクラスからオブジェクトを作成することはできません。
　吉里吉里のコンソールのログの名前は krkr.console.log になります。また、ハードウェア例外が発生したときに作成されるファイルは hwexcept.log となります。
　これらのログファイルは、デフォルトではプロジェクトディレクトリになります。ただし、プロジェクトディレクトリがアーカイブなど、書き込みができないディレクトリの場合は出力されません。
　ログファイルの出力先は logLocation プロパティで変更することができます (KAGの場合は栞データの保存先に設定されます)。

# メンバ

コンストラクタ
:   なし

メソッド
:   [addLoggingHandler](f_Debug_addLoggingHandler) ( ログハンドラを追加します )
    [getLastLog](f_Debug_getLastLog) ( 未出力のログを取得します )
    [logAsError](f_Debug_logAsError) ( エラー時と同じようにログをファイルに出力開始する )
    [message](f_Debug_message) ( コンソールへメッセージを出力 )
    [notice](f_Debug_notice) ( コンソールへ重要なメッセージを出力 )
    [removeLoggingHandler](f_Debug_removeLoggingHandler) ( ログハンドラを削除します )
    [startLogToFile](f_Debug_startLogToFile) ( コンソールのログの出力開始 )

プロパティ
:   [clearLogFileOnError](f_Debug_clearLogFileOnError) ( エラー発生時にコンソールのログファイルをクリアするかどうか )
    [logLocation](f_Debug_logLocation) ( ログファイルの出力先 )
    [logToFileOnError](f_Debug_logToFileOnError) ( エラー発生時にコンソールのログをファイルに出力するか )

イベント
:   なし