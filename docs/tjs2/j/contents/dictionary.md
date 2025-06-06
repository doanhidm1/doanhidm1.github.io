# Dictionary クラス

Dictionary クラスは辞書配列を扱うクラスです。

　辞書配列は連想配列とも呼ばれ、名前と、それに結びつけられた値を一つのペアとして、それを複数保持するオブジェクトです。
　配列と同じように [ ] (間接参照) 演算子でアクセスしますが、添え字の代わりに文字列を使い、それが名前となります。名前が識別子として有効なものであれば、 . (直接参照) 演算子も使うことができます。
　また、存在しない名前を参照すると void になります。
　要素を削除するには delete 演算子を使います。

`例:
    var d=new Dictionary();
    d["sat"] = 1; // d.sat = 1 と同じ
    d["sun"] = 2; // d.sun = 2 と同じ
    d["mon"] = 3; // d.mon = 3 と同じ
    d["name"] ="value!"; // d.name = "value!" と同じ
    d["continue"] = 4; // continue は識別子ではないが OK
    d.continue = 4; // continue は識別子ではないのでエラー

    var sat = d["sat"]; // 1 が代入される
    var none = d["none"]; // void が代入される

    delete d.sat; // sat を削除
    delete d["continue"]; // continue を削除`

# 式中辞書配列

`%[ ]` を使って、式中に `Dictionary` クラスのオブジェクトをその場で記述することができます。要素名 => 要素の値、をカンマで区切り、初期要素となる式を列挙します。たとえば、
`var dic = %["a" => 1, "b" => 2, "c" => 3];`　と記述すれば、`dic` に、要素名と要素の組がそれぞれ `"a":1`、 `"b":2`、 `"c":3` となる `Dictionary` クラスのオブジェクトへの参照が代入されます。
　内部的には、`=>` はカンマと全く同じものですが、読みやすさを考え、`=>` を使用できるようになっています ( perl と同じです )。

# Dictionary クラスのメソッドへのアクセス

Dictionary クラスのオブジェクトは、作成された状態ではメンバを何一つ持っていません。
　たとえば、assign メソッドを使おうと思って、Dictionary クラスのオブジェクト dict に対して`dict.assign(src)` のように記述しても、dict が assign というメソッドを持っていないためにエラーになります。
　したがって、incontextof 演算子を使って、Dictionary クラスに直接属しているメソッドを、対象となる Dictionary クラスのオブジェクトをコンテキストとして実行させます。

`例:
    var a = %[];
    var b = %[];
    (Dictionary.assign incontextof a)(b); // b を a にコピー
    (Dictionary.clear incontextof b)(); // b の内容をクリア`

# saveStruct

saveStruct はファイルへ構造化されたデータの出力を行います。
　[Array クラス](array) の同メソッド参照してください。

# assign

assign メソッドは、辞書配列をコピーします。

`構文 : assign(<コピー元辞書配列>, <内容をクリアするか=true>)`

　引数で指定された他の辞書配列の内容を、そっくりコピーします。
　「内容をクリアするか」が偽の場合は、コピー先 (メソッドを実行するオブジェクト) の内容をクリアせず、コピー元辞書配列の内容を上書きします。コピー元辞書配列と同じ名前のメンバがコピー先辞書配列にあった場合は、コピー元の内容でコピー先が上書きされます。

　配列 (Arrayクラスのオブジェクト) をコピー元配列に指定した場合は、その配列には、この辞書配列のメンバとなるべき要素が名前、値の順に並んでいるとみなし、その配列の内容をこの辞書配列にコピーします。

# assignStruct

assignStruct メソッドは、辞書配列をコピーします。

`構文 : assignStruct(<コピー元辞書配列>)`

　引数で指定された他の辞書配列の内容を、そっくりコピーします。
　assign メソッドと違い、メンバに配列あるいは辞書配列があった場合は、再帰的にその内容も
コピーします ( assign メソッドの場合は参照がコピーされるだけです )。

# clear

clear メソッドは、辞書配列の内容をすべて消去します。