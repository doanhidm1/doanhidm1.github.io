# LineParser.parse

機能/意味
:   テキストに対するパース処理を実行する。

タイプ
:   [LineParserクラス](class_LineParser)のメソッド

構文
:   parse(text)

引数
:   |  |  |
    | --- | --- |
    | text | テキスト。省略時は現在設定中のテキストに対して処理を行なう |

戻り値
:   なし (void)

説明
:   行ごとに doLine() イベントを呼び出す。