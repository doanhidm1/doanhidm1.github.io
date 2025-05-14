# Storages.getTime

機能/意味
:   タイムスタンプ取得

タイプ
:   [Storagesクラス](class_Storages)のメソッド

構文
:   getTime(target)

引数
:   |  |  |
    | --- | --- |
    | target | 対象ファイルまたはディレクトリ |

戻り値
:   タイムスタンプ情報の入った辞書\nmtime: 更新日時 (Date オブジェクト)\natime: アクセス日時 (Date オブジェクト)\nctime: 作成日時 (Date オブジェクト)\n⇒fstatとの違いは非アーカイブファイル限定で，sizeを返さないこと

説明