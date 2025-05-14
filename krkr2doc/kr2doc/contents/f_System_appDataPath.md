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

    Windows 95, 98, 98SE, ME でマルチユーザ環境でない場合
    :   C:\Windows\Application Data\ ( C:\Windows の部分は Windows をインストールした場所です )

    Windows 95 (初期型でない場合), 98, 98SE, ME でマルチユーザ環境の場合
    :   C:\Windows\Profiles\<ユーザ名>\Application Data\ ( C:\Windows の部分は Windows をインストールした場所です )

    Windows NT 4.0 の場合
    :   C:\WINNT\Profiles\<ユーザ名>\Application Data\ ( C:\WINNT の部分は Windows をインストールした場所です )

    Windows 2000, XP 以降 の場合
    :   C:\Documents and Settings\<ユーザ名>\Application Data\ ( C: の部分は環境によって異なります )

    何らかの理由で レジストリキー ( 上記参照 ) を読み出せなかった場合か、初期の Windows 95
    :   吉里吉里の実行可能ファイルのあるフォルダ ([System.exePath](f_System_exePath))になります

参照
:   [System.exePath](f_System_exePath)
    [System.personalPath](f_System_personalPath)