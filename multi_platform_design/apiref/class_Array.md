# Array

Array クラスは配列を扱うクラスです。

このクラスのオブジェクトを作成し、間接メンバ選択演算子によって指定された添え字を使って配列のように扱うことができます。
添え字は整数です。
0は先頭の要素を表し、1はその次の要素を表します。
負の整数を指定すると、配列の最後から指定したものとして扱われます (-1 は最後の要素を表します)。
配列の大きさは宣言する必要はありません。
指定された添え字の大きさまで自動的にサイズが拡張され、何も値が代入されていない要素は void に初期化されます。

また、count プロパティがあり、これが配列のサイズを表しています。
count プロパティに値を代入しても配列のサイズを変えることができます。

[ ] を使って、式中に Array クラスのオブジェクトをその場で記述することができます。
[ ] にはカンマで区切り、初期要素となる式を列挙します。
たとえば、
`var ar = ["a", "b", "c"];`
と記述すれば、ar に、 "a" "b" "c" の要素が入った Array クラスのオブジェクトへの参照が代入されます。
また、Array クラスを生成する場合も [ ] を使うことができます。
`var ar = [];`
と
`var ar = new Array();`
は同じです。

# メンバ

メソッド
:   [add](func_Array_add) (指定された値を配列の最後に追加します。 )
    [assign](func_Array_assign) (配列をコピーします。 )
    [assignStruct](func_Array_assignStruct) (配列を構造ごとコピーします。 )
    [clear](func_Array_clear) (配列の要素をすべて削除します。 )
    [erase](func_Array_erase) (指定された添え字の要素を削除します。 )
    [find](func_Array_find) (指定された値が最初に現れる添え字を返します。 )
    [forEach](func_Array_forEach) (引数の関数を、配列の各要素に対して実行します。 )
    [includes](func_Array_includes) (指定された値を含んでいるかどうか判定します。 )
    [insert](func_Array_insert) (指定された値を指定された位置に挿入します。 )
    [join](func_Array_join) (配列を結合し、一つの文字列にします。 )
    [load](func_Array_load) (配列をファイルから読み込みます。 )
    [loadStruct](func_Array_loadStruct) (ファイルから構造化されたデータの入力を行います )
    [pack](func_Array_pack) (引数で指定された文字列に従い、配列要素をバイナリ(Octet)化して返します。 )
    [pop](func_Array_pop) (配列の最後から一つ要素を取り出し、それを返します。 )
    [push](func_Array_push) (指定された要素を配列の最後に追加します。 )
    [remove](func_Array_remove) (指定された値と同じ値を持つ要素を削除します。 )
    [reverse](func_Array_reverse) (配列の要素の並びを逆さまにします。 )
    [save](func_Array_save) (配列をファイルに書き出します。 )
    [saveStruct](func_Array_saveStruct) (ファイルへ構造化されたデータの出力を行います。 )
    [shift](func_Array_shift) (配列の最初から一つ要素を取り出し、それを返します。 )
    [sort](func_Array_sort) (配列をソート(並び替え)します。 )
    [split](func_Array_split) (文字列を分割します。 )
    [unshift](func_Array_unshift) (要素を配列の先頭に追加します。 )

プロパティ
:   [count](prop_Array_count) (配列の大きさを表します。 )
    [length](prop_Array_length) (配列の大きさを表します。countと同じです。 )

イベント