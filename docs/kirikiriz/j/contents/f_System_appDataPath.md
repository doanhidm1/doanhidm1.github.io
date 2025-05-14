# System.appDataPath

機能/意味
:   ユーザのホームディレクトリのパス

タイプ
:   [Systemクラス](f_System)のプロパティ (読み出し専用)

説明
:   ユーザのホームディレクトリのパスを表します。Windows の場合、レジストリの
    HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Shell Folders の
    AppData で表されるフォルダが返されます。このフォルダがない場合は [System.exePath](f_System_exePath) と同じ
    フォルダを返します。

    これは、通常、以下の通りになります。

    XP の場合
    :   C:\Documents and Settings\<ユーザ名>\Application Data\ ( C: の部分は環境によって異なります )

    Vista, 7, 8 の場合
    :   C:\Users\<ユーザ名>\AppData\Roaming ( C: の部分は環境によって異なります )

    何らかの理由で レジストリキー ( 上記参照 ) を読み出せなかった場合
    :   吉里吉里の実行可能ファイルのあるフォルダ ([System.exePath](f_System_exePath))になります

参照
:   [System.exePath](f_System_exePath)
    [System.personalPath](f_System_personalPath)