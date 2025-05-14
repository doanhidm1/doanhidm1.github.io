# Scripts.setCallMissing

機能/意味
:   missingメソッドの呼び出し設定

タイプ
:   [Scriptsクラス](class_Scripts)のメソッド

構文
:   setCallMissing(obj)

引数
:   |  |  |
    | --- | --- |
    | obj | メンバが見つからない時にmissingメソッドが呼び出されるようにするオブジェクト。 |

戻り値
:   なし (void)

説明
:   メンバが見つからない時にmissingメソッドが呼び出されるように設定します。
    このメソッドで登録したオブジェクトでメンバが見つからない場合、function missing( isset, name, prop ) の形式でメソッドが呼び出されます。
    isset は、true なら設定、false なら取得です。
    name は見付からなかったメンバの名前です。
    prop は設定時は代入される値、取得時は返す値の代入先です。
    nameメンバがmissingメソッドでも見付からない場合は、0以外の値を返します。
    0以外を返すとメンバが見付からないという例外が発生します。
    関数が見付からない場合でも、getで呼び出されます。
    finalize関数も対象なので、この設定をするクラスにはfinalize関数を定義しておいた方が良いです。