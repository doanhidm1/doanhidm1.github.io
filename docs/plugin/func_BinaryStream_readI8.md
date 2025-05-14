# BinaryStream.readI8

機能/意味
:   {1,2,4,8}バイトを数値として読み込む

タイプ
:   [BinaryStreamクラス](class_BinaryStream)のメソッド

構文
:   readI8()

引数

戻り値
:   読み込んだ数値 / 終端などで読めなかった場合はvoid

説明
:   ※数値は8byte以外はunsigned読み込みになります（符号拡張されません）
    ※voidを返すのは1byteも読めなかった場合のみとなります
    1byte以上指定byte未満しか読めなかった場合は足りない部分を0で埋めた値が返されるので注意