# Storages.copyFileNoNormalize

機能/意味
:   パスの正規化を行なわず吉里吉里のストレージ空間中の指定ファイルをコピーする (コピー先ファイルのファイル名が小文字に変換されない)

タイプ
:   [Storagesクラス](class_Storages)のメソッド

構文
:   copyFileNoNormalize(from, to, failIfExist)

引数
:   |  |  |
    | --- | --- |
    | from | コピー元ファイル |
    | to | コピー先ファイル |
    | failIfExist | ファイルが存在するときに失敗するなら ture、上書きするなら false |

戻り値
:   実際にコピーできたら true

説明