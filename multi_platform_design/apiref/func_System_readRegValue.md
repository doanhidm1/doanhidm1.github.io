# System.readRegValue

機能/意味
:   [Windows+]レジストリの読み込み

タイプ
:   [Systemクラス](class_System)のメソッド

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
    HKEY*CLASSES*ROOTHKEY*CURRENT*CONFIGHKEY*CURRENT*USERHKEY*LOCAL*MACHINEHKEY*USERSHKEY*PERFORMANCE*DATAHKEY*DYN*DATA
    たとえば、以下のような文字列を key に指定することができます。
    HKEY*LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\hoeg\installdir
    数値、単一文字列のみを読み込むことができます。
    数値の場合は整数型、文字列の場合は文字列型の結果が返ります。