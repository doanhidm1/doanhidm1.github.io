# System.createUUID

機能/意味
:   UUID 文字列の生成

タイプ
:   [Systemクラス](class_System)のメソッド

構文
:   createUUID()

引数

戻り値
:   生成された UUID 文字列が "e8b2a2b5-5ceb-4f75-a08b-1f1bdfdca4f1" の形式(ハイフンを除く各英数字は16進数の数字) で戻ります。

説明
:   UUID 文字列を生成して返します。このメソッドはランダムビット列を元に生成された128bitの UUID (universal unique identifier) を生成します。
    吉里吉里に実装されている UUID 生成アルゴリズムは、ある程度、環境ノイズを拾ってランダムビット列を生成しますが、高度なセキュリティが要求されるような用途に使用することはおすすめしません。
    しかし、他の UUID とは「非常に非常に高い確率で重ならない」と考えられます。