# System.getDoubleClickTime

機能/意味
:   システムのダブルクリック許容時間を取得

タイプ
:   [Systemクラス](class_System)のメソッド

構文
:   getDoubleClickTime()

引数

戻り値
:   時間(ms) 既定値は500ms

説明
:   詳細は GetDoubleClickTime() API のマニュアルを参照
    ダブルクリックの許容移動範囲はgetSystemMetricsのCXDOUBLECLK/CYDOUBLECLKで取得可能
    Layer.onDoubleClickを使わずにソフトウェアで擬似的にダブルクリック判定を行う場合に使用（時間決め打ちでも問題ないけど一応…）