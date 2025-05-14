# KAGParser.onScenarioLoad

機能/意味
:   シナリオ読み込みが開始した

タイプ
:   [KAGParserクラス](f_KAGParser)のイベント

構文
:   onScenarioLoad(storage)

引数
:   |  |  |
    | --- | --- |
    | storage | 読み込まれるシナリオストレージの名前が渡されます。 |

説明
:   シナリオ読み込みを開始する時に呼ばれます。
    　このイベントで文字列を返すと、ストレージ storage の中身の代わりに
    その文字列をシナリオとして用います。

参照
:   [KAGParser.loadScenario](f_KAGParser_loadScenario)
    [KAGParser.onScenarioLoaded](f_KAGParser_onScenarioLoaded)