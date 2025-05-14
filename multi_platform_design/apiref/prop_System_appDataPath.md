# System.appDataPath

機能/意味
:   ユーザのホームディレクトリのパス

タイプ
:   [Systemクラス](class_System)のプロパティ

説明
:   ユーザのホームディレクトリのパスを表します。
    Windows の場合、レジストリのHKEY*CURRENT*USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Shell Folders のAppData で表されるフォルダが返されます。
    このフォルダがない場合は System.exePath と同じフォルダを返します。
    これは、通常、以下の通りになります。
    XP の場合C:\Documents and Settings\<ユーザ名>\Application Data\ ( C: の部分は環境によって異なります )
    Vista, 7, 8 の場合C:\Users\<ユーザ名>\AppData\Roaming ( C: の部分は環境によって異なります )何らかの理由で レジストリキー ( 上記参照 ) を読み出せなかった場合吉里吉里の実行可能ファイルのあるフォルダ (System.exePath)になります
    AndroidではfilesDirと同じです。

参照
:   [System.exePath](prop_System_exePath)
    [System.personalPath](prop_System_personalPath)
    [System.filesDir](prop_System_filesDir)