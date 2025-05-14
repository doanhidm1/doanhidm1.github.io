# System.getSystemMetrics

機能/意味
:   システムメトリクス情報を取得

タイプ
:   [Systemクラス](class_System)のメソッド

構文
:   getSystemMetrics(index)

引数
:   |  |  |
    | --- | --- |
    | index | SM\_\* の「\*」部分の文字列（ただし大文字小文字は無関係） |

戻り値
:   メトリクス値（indexにより内容が異なる）

説明
:   詳細は GetSystemMetrics() API のマニュアルを参照
    SW\_ARRANGE は ARW\_\* の定義がないので直接数値指定で比較すること