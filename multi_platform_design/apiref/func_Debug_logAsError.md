# Debug.logAsError

機能/意味
:   エラー時と同じようにログをファイルに出力開始する

タイプ
:   [Debugクラス](class_Debug)のメソッド

構文
:   logAsError()

引数

戻り値
:   なし (void)

説明
:   エラーログファイルに関し、吉里吉里がエラーが発生したときと同じ動作をさせます。
    つまり、Debug.logToFileOnError が真ならばファイルにコンソールのログの出力を開始します。
    その際、Debug.clearLogFileOnError が真ならばファイルをクリアします。
    これに対し、Debug.startLogToFile は無条件でコンソールのログのファイルへの出力を開始します。

参照
:   [Debug.startLogToFile](func_Debug_startLogToFile)
    [Debug.logToFileOnError](prop_Debug_logToFileOnError)
    [Debug.clearLogFileOnError](prop_Debug_clearLogFileOnError)