# Scripts.saveSQ

機能/意味
:   データを Squirrel 形式で保存する。このファイルは "return" を先頭にもつので dofile() で読みだすことができます

タイプ
:   [Scriptsクラス](class_Scripts)のメソッド

構文
:   saveSQ(filename, obj, utf8, newline)

引数
:   |  |  |
    | --- | --- |
    | filename | 格納先ファイル |
    | obj | 保存対象オブジェクト |
    | utf8 | 出力エンコーディング指定。true なら UTF-8、falseなら現在のコードページ |
    | newline | 改行コード 0:CRLF 1:LF |

戻り値
:   なし (void)

説明