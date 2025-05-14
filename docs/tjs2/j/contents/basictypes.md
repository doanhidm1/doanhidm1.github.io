# プリミティブ型

tjsTypes.h で定義されているプリミティブ型がいくつかあります。

tjs\_int
:   符号あり整数(最低32bit)

tjs\_uint
:   符号なし整数(最低32bit)

tjs\_int8
:   8bitの符号あり整数

tjs\_uint8
:   8bitの符号なし整数

tjs\_int16
:   16bitの符号あり整数

tjs\_uint16
:   16bitの符号なし整数

tjs\_int32
:   32bitの符号あり整数

tjs\_uint32
:   32bitの符号なし整数

tjs\_int64
:   64bitの符号あり整数

tjs\_uint64
:   64bitの符号なし整数

tjs\_char
:   ワイド文字(TJS2の文字列型のプリミティブ型として使用されます)

tjs\_nchar
:   ナロー文字

tjs\_real
:   実数型(double)

tTVInteger
:   tjs\_int64と同じ

tTVReal
:   tjs\_realと同じ

# tTJSString

tTJSString 型は TJS2 で用いる文字列型で、tjs\_char 型のゼロ終結文字列を扱います。tjsString.cpp / tjsString.h に定義されています。また、短く `ttstr` という型名でも利用可能です。
　この型は文字列用のメモリの管理を自動的に行うほか、[tTJSVariant 型](variant) との親和性が高い型です。

# eTJS

eTJS 型は C++ 例外オブジェクトの基本型です。tjsError.h に定義されています。GetMessage というメソッドがあり、例外とともに投げられたメッセージ文字列を取得することができます。

# TJS\_W

文字列リテラルを tjs\_char \* 型に変換するためのマクロです。

例 : TJS\_W("文字列リテラル")