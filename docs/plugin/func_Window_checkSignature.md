# Window.checkSignature

機能/意味
:   署名チェックの開始

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   checkSignature(filename, publickey, info)

引数
:   |  |  |
    | --- | --- |
    | filename | 確認対象ファイル |
    | publickey | 公開鍵 |
    | info | ユーザ情報 |

戻り値
:   handler 識別ハンドラ

説明
:   処理中に onCheckSignatureProgress、
    終了時に onCheckSignatureDone イベントが発生します。
    exe や dll の場合は署名はファイルに内臓されます。xp3 などの場合は、
    元のファイルに .sig をつけた外部ファイルを署名として処理されます。