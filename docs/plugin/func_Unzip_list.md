# Unzip.list

機能/意味
:   ZIPアーカイブ中に含まれるファイルの情報を取得します

タイプ
:   [Unzipクラス](class_Unzip)のメソッド

構文
:   list()

引数

戻り値
:   ファイル一覧(ファイル情報の配列)\nファイル情報は辞書の形で、以下の情報を含みます\n

    \n

    filename: アーカイブ内パス名\n uncompressed\_size: 展開サイズ\n compressed\_size: 圧縮サイズ\n crypted: 暗号化されているか\n deflated: 圧縮されているか\n deflateLevel: 圧縮レベル\n crc: ファイルのCRD\n

説明