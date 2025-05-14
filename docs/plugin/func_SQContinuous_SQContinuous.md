# SQContinuous.SQContinuous

機能/意味
:   コンストラクタ

タイプ
:   [SQContinuousクラス](class_SQContinuous)のメソッド

構文
:   SQContinuous(func)

引数
:   |  |  |
    | --- | --- |
    | func | squirrel のグローバルな関数 func(tick){} の名前 ※tick は SQInteger にキャストされてから呼び出されます |

戻り値
:   なし (void)

説明
:   このメソッドによる実行中では Object/Thread 拡張による wait は利用できません