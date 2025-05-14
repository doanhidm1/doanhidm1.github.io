# System.personalPath

機能/意味
:   マイドキュメントのパス

タイプ
:   [Systemクラス](f_System)のプロパティ (読み出し専用)

説明
:   ユーザのマイドキュメントのパスを表します。Windows の場合、レジストリの
    HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Shell Folders の
    Personal で表されるフォルダが返されます。通常これは「マイドキュメント」フォルダを指します。
    このフォルダがない場合は [System.exePath](f_System_exePath) と同じフォルダを返します。

参照
:   [System.appDataPath](f_System_appDataPath)
    [System.exePath](f_System_exePath)