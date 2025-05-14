# KAGParser.getNextTag

機能/意味
:   次のタグを得る

タイプ
:   [KAGParserクラス](f_KAGParser)のメソッド

構文
:   getNextTag()

引数
:   なし

戻り値
:   タグ情報の辞書配列

説明
:   次のタグを辞書配列で返します。(タグ内部にない)通常の文字は、ch タグと解釈されます。
    　interrupted 状態では、interrupt タグを返し、interrupted 状態を解除します。
    　ストレージの末尾では、void を返します。
    　タグの名前は、戻り値の辞書配列の tagname 要素に格納されています。
    　if, ignore, endif, endignore, emb, macro, endmacro, erasemacro,
    jump, call, return, iscript, endscript の各タグは組み込みタグです。
    これらのタグに関する処理は、このメソッドの内部で自動的に行なわれます。
    したがって、このメソッドはこれらのタグに関する情報を返しません。

参照
:   [KAGParser.interrupt](f_KAGParser_interrupt)
    [KAGParser.resetInterrupt](f_KAGParser_resetInterrupt)