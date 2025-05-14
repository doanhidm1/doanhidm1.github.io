# Debug.logAsError

機能/意味
:   エラー時と同じようにログをファイルに出力開始する

タイプ
:   [Debugクラス](f_Debug)のメソッド

構文
:   logAsError()

引数
:   なし

戻り値
:   なし (void)

説明
:   エラーログファイルに関し、吉里吉里がエラーが発生したときと同じ動作をさせます。
    つまり、
    [Debug.logToFileOnError](f_Debug_logToFileOnError) が真ならばファイルにコンソールのログの出力を
    開始します。その際、[Debug.clearLogFileOnError](f_Debug_clearLogFileOnError) が真ならばファイルを
    クリアします。
    　これに対し、[Debug.startLogToFile](f_Debug_startLogToFile) は無条件でコンソールのログの
    ファイルへの出力を開始します。

参照
:   [Debug.startLogToFile](f_Debug_startLogToFile)
    [Debug.logToFileOnError](f_Debug_logToFileOnError)
    [Debug.clearLogFileOnError](f_Debug_clearLogFileOnError)