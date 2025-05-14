# String

TJS2 では、文字列は擬似的に String クラスのオブジェクトということになっていますが、String クラスは存在していませんし、実際に String クラスのオブジェクトというわけではありません ( ただし 文字列に対して typeof 演算子を使うと "String" を返します )。
しかし 文字列をオブジェクトと見立てて、いくつかのメソッドやプロパティが使用可能になっています。

# メンバ

メソッド
:   [charAt](func_String_charAt) (文字列の指定位置で指定された位置の文字を返します )
    [endsWith](func_String_endsWith) (文字列が指定された部分文字列で終了しているかどうかを返します )
    [escape](func_String_escape) (文字列を、TJSの文字列即値内で表現可能な形式に変換します )
    [indexOf](func_String_indexOf) (部分文字列の位置を返します )
    [repeat](func_String_repeat) (指定した回数だけ文字列を繰り返した文字列を返します )
    [replace](func_String_replace) (文字列の置き換えを行います )
    [reverse](func_String_reverse) (文字の並びを逆転した文字列を返します )
    [split](func_String_split) (文字列を分割します )
    [sprintf](func_String_sprintf) (文字列を書式化します )
    [startsWith](func_String_startsWith) (文字列が指定された部分文字列で開始されているかどうかを返します )
    [substr](func_String_substr) (文字列の部分文字列を返します )
    [substring](func_String_substring) (文字列の部分文字列を返します )
    [toLowerCase](func_String_toLowerCase) (文字列のアルファベットを小文字にした文字列を返します )
    [toUpperCase](func_String_toUpperCase) (小文字のアルファベットを大文字にした文字列を返します )
    [trim](func_String_trim) (文字列の先頭と最後の空白を取り除いた文字列を返します )

プロパティ
:   [［］](prop_String_%EF%BC%BB%EF%BC%BD) ('数値' プロパティ )
    [length](prop_String_length) (文字列の長さを返します )

イベント