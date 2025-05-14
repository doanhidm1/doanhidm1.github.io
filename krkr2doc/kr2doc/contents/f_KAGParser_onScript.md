# KAGParser.onScript

機能/意味
:   iscript ブロックを通過した

タイプ
:   [KAGParserクラス](f_KAGParser)のイベント

構文
:   onScript(script, storageShortName, scriptStart)

引数
:   |  |  |
    | --- | --- |
    | script | iscript タグと endscript タグで挟まれた部分が文字列として渡されます。 |
    | storageShortName | 短いストレージ名が渡されます。 |
    | scriptStart | スクリプト開始行の行数が渡されます。 |

説明
:   [KAGParser.getNextTag](f_KAGParser_getNextTag) メソッドが、iscript ... endscript の部分を通過したときに呼ばれます。
    　eval タグでは呼ばれません。
    　[KAGParser.getNextTag](f_KAGParser_getNextTag) メソッドは、iscript ... endscript の部分に関する情報は返さず、
    この部分をスキップします。したがって、iscript ... endscript の中身の処理は、このイベント内で
    する必要があります。

参照
:   [KAGParser.getNextTag](f_KAGParser_getNextTag)