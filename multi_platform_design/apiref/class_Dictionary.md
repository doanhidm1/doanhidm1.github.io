# Dictionary

Dictionary クラスは辞書配列を扱うクラスです。

辞書配列は連想配列とも呼ばれ、名前と、それに結びつけられた値を一つのペアとして、それを複数保持するオブジェクトです。
配列と同じように [ ] (間接参照) 演算子でアクセスしますが、添え字の代わりに文字列を使い、それが名前となります。
名前が識別子として有効なものであれば、 . (直接参照) 演算子も使うことができます。
また、存在しない名前を参照すると void になります。
要素を削除するには delete 演算子を使います。

# 式中辞書配列

%[ ] を使って、式中に Dictionary クラスのオブジェクトをその場で記述することができます。
要素名 => 要素の値、をカンマで区切り、初期要素となる式を列挙します。たとえば、

`var dic = %["a" => 1, "b" => 2, "c" => 3];`

と記述すれば、dic に、要素名と要素の組がそれぞれ "a":1、 "b":2、 "c":3 となる Dictionary クラスのオブジェクトへの参照が代入されます。
内部的には、=> はカンマと全く同じものですが、読みやすさを考え、=> を使用できるようになっています ( perl と同じです )。

# Dictionary クラスのメソッドへのアクセス

Dictionary クラスのオブジェクトは、作成された状態ではメンバを何一つ持っていません。
たとえば、assign メソッドを使おうと思って、Dictionary クラスのオブジェクト dict に対してdict.assign(src) のように記述しても、dict が assign というメソッドを持っていないためにエラーになります。
したがって、incontextof 演算子を使って、Dictionary クラスに直接属しているメソッドを、対象となる Dictionary クラスのオブジェクトをコンテキストとして実行させます。

例:
 `var a = %[];
var b = %[];
(Dictionary.assign incontextof a)(b); // b を a にコピー
(Dictionary.clear incontextof b)(); // b の内容をクリア`

# メンバ

メソッド
:   [assign](func_Dictionary_assign) (辞書配列をコピーします )
    [assignStruct](func_Dictionary_assignStruct) (辞書配列をコピーします )
    [clear](func_Dictionary_clear) (辞書配列の内容をすべて消去します )
    [contains](func_Dictionary_contains) (辞書配列に指定された key が存在するか判定します。 )
    [forEach](func_Dictionary_forEach) (引数の関数を、引数の辞書配列の各要素に対して実行します。 )
    [getCount](func_Dictionary_getCount) (オブジェクトのメンバの数を返します。 )
    [keys](func_Dictionary_keys) (オブジェクトのキーの配列を返します。 )
    [loadStruct](func_Dictionary_loadStruct) (ファイルから構造化されたデータの入力を行います )
    [saveStruct](func_Dictionary_saveStruct) (ファイルへ構造化されたデータの出力を行います )
    [values](func_Dictionary_values) (オブジェクトの値の配列を返します。 )

プロパティ

イベント