# Scripts.compileStorage

機能/意味
:   ストレージ上のスクリプトのコンパイル

タイプ
:   [Scriptsクラス](f_Scripts)のメソッド

構文
:   compileStorage(inputfile, outputfile, isresult=false, outputdebug=false, isexpression=false)

引数
:   |  |  |
    | --- | --- |
    | inputfile | コンパイル対象ストレージを指定します。 |
    | outputfile | 出力バイトコードストレージを指定します。 |
    | isresult | 戻り値が必要かどうかを指定します。 |
    | outputdebug | デバッグ情報を含めるかどうかを指定します。 |
    | isexpression | 式かどうかを指定します。 |

戻り値
:   なし (void)

説明
:   指定されたストレージを読み込み、その内容をコンパイルしてバイトコードファイルとして出力します。
    　コンパイルされたバイトコードファイルは execStorage もしくは、evalStorage で通常のスクリプトと同じように実行できます。

参照
:   [Scripts.execStorage](f_Scripts_execStorage)
    [Scripts.evalStorage](f_Scripts_evalStorage)