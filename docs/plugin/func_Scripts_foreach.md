# Scripts.foreach

機能/意味
:   オブジェクトのメンバの全参照

タイプ
:   [Scriptsクラス](class_Scripts)のメソッド

構文
:   foreach(obj, func, args)

引数
:   |  |  |
    | --- | --- |
    | obj | 処理対象オブジェクト(辞書または配列) |
    | func | 呼び出し関数。func(key, value, args\*) の形で呼ばれます。 無名関数などコンテキストが null の場合は自動的に thisコンテキストで動作します 関数がなにかしら値を返すと処理が中断されます |
    | args | 追加引数 配列の場合は単純にループによる参照になります。辞書やオブジェクトは iTJSDispatch2::EnumMebers の呼び出しになります |

戻り値
:   中断時に返された値

説明