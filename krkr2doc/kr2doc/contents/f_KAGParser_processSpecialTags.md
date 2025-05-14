# KAGParser.processSpecialTags

機能/意味
:   特殊タグを処理するかどうか

タイプ
:   [KAGParserクラス](f_KAGParser)のプロパティ (読み書き可能)

説明
:   特殊タグを処理するかどうかを表わします。
    　真ならば改行を特殊タグを処理します。デフォルトは真です。
    　特殊タグとは if ignore endif endignore else elsif emb macro endmacro macropop erasemacro jump call return の各タグです。このプロパティが偽の場合、これらのタグはそのまま getNextTag で取得することができます。
    　ただし、iscript ～ endscript は常に処理されます。