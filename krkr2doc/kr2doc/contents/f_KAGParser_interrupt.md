# KAGParser.interrupt

機能/意味
:   interrupted 状態にする

タイプ
:   [KAGParserクラス](f_KAGParser)のメソッド

構文
:   interrupt()

引数
:   なし

戻り値
:   なし (void)

説明
:   interrupted 状態になります。この状態のときは、
    次の [KAGParser.getNextTag](f_KAGParser_getNextTag) メソッドの呼び出しでは interrupt タグが返されます。

参照
:   [KAGParser.resetInterrupt](f_KAGParser_resetInterrupt)
    [KAGParser.getNextTag](f_KAGParser_getNextTag)