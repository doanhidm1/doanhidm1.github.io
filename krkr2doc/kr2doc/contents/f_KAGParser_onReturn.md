# KAGParser.onReturn

機能/意味
:   return タグが呼ばれた

タイプ
:   [KAGParserクラス](f_KAGParser)のイベント

構文
:   onReturn(dic)

引数
:   |  |  |
    | --- | --- |
    | dic | return タグの情報を持つ辞書配列 |

説明
:   [KAGParser.getNextTag](f_KAGParser_getNextTag) メソッドが return タグを読んだときに呼ばれます。
    　このイベントで偽を返すと、移動は行なわれません。

参照
:   [KAGParser.getNextTag](f_KAGParser_getNextTag)