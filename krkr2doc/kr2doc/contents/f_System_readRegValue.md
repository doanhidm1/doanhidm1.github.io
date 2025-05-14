# System.readRegValue

機能/意味
:   レジストリの読み込み

タイプ
:   [Systemクラス](f_System)のメソッド

構文
:   readRegValue(key)

引数
:   |  |  |
    | --- | --- |
    | key | 読み込むレジストリキーを指定します。 |

戻り値
:   実行に成功すればレジストリの値、失敗すれば void が返ります。

説明
:   key で指定した Windows レジストリを読み込みます。
    　レジストリキーは、以下のルートキー名で始めることができます。
    HKEY\_CLASSES\_ROOT
    HKEY\_CURRENT\_CONFIG
    HKEY\_CURRENT\_USER
    HKEY\_LOCAL\_MACHINE
    HKEY\_USERS
    HKEY\_PERFORMANCE\_DATA
    HKEY\_DYN\_DATA
     　たとえば、以下のような文字列を key に指定することができます。
    HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\hoeg\installdir

    　数値、単一文字列のみを読み込むことができます。数値の場合は整数型、文字列の場合は文字列型
    の結果が返ります。