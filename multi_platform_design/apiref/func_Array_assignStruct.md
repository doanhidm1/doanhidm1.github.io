# Array.assignStruct

機能/意味
:   配列を構造ごとコピーします。

タイプ
:   [Arrayクラス](class_Array)のメソッド

構文
:   assignStruct(src:Array)

引数
:   |  |  |
    | --- | --- |
    | src | コピー元のArray|Dictionaryインスタンス |

戻り値
:   なし (void)

説明
:   引数で指定された他の配列の内容を、そっくりコピーします。
    assign メソッドと違い、メンバに配列あるいは辞書配列があった場合は、再帰的にその内容も コピーします ( assign メソッドの場合は参照がコピーされるだけです )。