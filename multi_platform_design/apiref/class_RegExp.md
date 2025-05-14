# RegExp

RegExp クラスは正規表現パターンを扱うクラスです。
正規表現パターンには perl 互換のパターンを指定することができます。
JavaScript の RegExp クラスににていますが、互換性は低いです。

# Copyright notice

正規表現機能の実装には K.Kosako 氏の鬼車を用いています。
有用なライブラリを公開なさっている氏に感謝します。

# 正規表現パターン

/ と / で囲まれた部分に正規表現パターンを指定することができます。
トークン を参照してください。

# メンバ

コンストラクタ
:   [RegExp](func_RegExp_RegExp) (コンストラクタ )

メソッド
:   [compile](func_RegExp_compile) (正規表現オブジェクトに新しい正規表現パターンを設定します )
    [exec](func_RegExp_exec) (引数に指定した文字列に正規表現パターンマッチングを行い、マッチした結果を含む配列を返します )
    [match](func_RegExp_match) (引数に指定した文字列に正規表現パターンマッチングを行い、マッチした結果を含む配列を返します )
    [replace](func_RegExp_replace) (文字列の置き換えを行い、置き換えが行われた後の文字列を返します )
    [split](func_RegExp_split) (文字列を分割します )
    [test](func_RegExp_test) (引数に指定した文字列がパターンにマッチするかどうかを返します )

プロパティ
:   [index](prop_RegExp_index) (マッチした部分の先頭文字の位置を表す、読み出し専用のプロパティです )
    [input](prop_RegExp_input) (マッチング対象の文字列をあらわす、読み出し専用のプロパティです )
    [last](prop_RegExp_last) (最後に test あるいは exec メソッドが実行された RegExp クラスのインスタンスです )
    [lastIndex](prop_RegExp_lastIndex) (マッチした部分の最終文字の次の文字の位置を表す、読み出し専用のプロパティです )
    [lastMatch](prop_RegExp_lastMatch) (マッチング対象文字列を表します )
    [lastParen](prop_RegExp_lastParen) (マッチした各部分のうち、最後の部分を返します )
    [leftContext](prop_RegExp_leftContext) (マッチング対象文字列のうち、マッチした部分よりも左側の文字列をあらわす、読み出し専用のプロパティです )
    [matches](prop_RegExp_matches) (マッチした各部分を含む配列を表す読み出し専用のプロパティです )
    [rightContext](prop_RegExp_rightContext) (マッチング対象文字列のうち、マッチした部分よりも右側の文字列をあらわす、読み出し専用のプロパティです )
    [start](prop_RegExp_start) (文字列の検索開始位置を表すプロパティです )

イベント