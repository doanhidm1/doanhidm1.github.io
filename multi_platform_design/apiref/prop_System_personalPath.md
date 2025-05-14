# System.personalPath

機能/意味
:   マイドキュメントのパス

タイプ
:   [Systemクラス](class_System)のプロパティ

説明
:   ユーザのマイドキュメントのパスを表します。
    Windows の場合、レジストリのHKEY*CURRENT*USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Shell Folders のPersonal で表されるフォルダが返されます。
    通常これは「マイドキュメント」フォルダを指します。
    このフォルダがない場合は System.exePath と同じフォルダを返します。

参照
:   [System.appDataPath](prop_System_appDataPath)
    [System.exePath](prop_System_exePath)