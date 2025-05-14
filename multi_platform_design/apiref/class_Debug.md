# Debug

Debug クラスは 吉里吉里のデバッグに関する機能を提供するクラスです。
このクラスからオブジェクトを作成することはできません。
吉里吉里のコンソールのログの名前は krkr.console.log になります。
また、ハードウェア例外が発生したときに作成されるファイルは hwexcept.log となります。
これらのログファイルは、デフォルトではプロジェクトディレクトリになります。
ただし、プロジェクトディレクトリがアーカイブなど、書き込みができないディレクトリの場合は出力されません。
ログファイルの出力先は logLocation プロパティで変更することができます (KAGの場合は栞データの保存先に設定されます)。
Windowsではコンソールはコマンドプロンプト、AndroidではlogCatへの出力となります。

# メンバ

メソッド
:   [addLoggingHandler](func_Debug_addLoggingHandler) (ログハンドラを追加します )
    [getLastLog](func_Debug_getLastLog) (未出力のログを取得します )
    [logAsError](func_Debug_logAsError) (エラー時と同じようにログをファイルに出力開始する )
    [message](func_Debug_message) (コンソールへメッセージを出力 )
    [notice](func_Debug_notice) (コンソールへ重要なメッセージを出力 )
    [removeLoggingHandler](func_Debug_removeLoggingHandler) (ログハンドラを削除します )
    [startLogToFile](func_Debug_startLogToFile) (コンソールのログの出力開始 )

プロパティ
:   [clearLogFileOnError](prop_Debug_clearLogFileOnError) (エラー発生時にコンソールのログファイルをクリアするかどうか )
    [logLocation](prop_Debug_logLocation) (ログファイルの出力先 )
    [logToFileOnError](prop_Debug_logToFileOnError) (エラー発生時にコンソールのログをファイルに出力するか )

イベント