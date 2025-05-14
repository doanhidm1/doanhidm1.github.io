# System.getKeyState

機能/意味
:   [Windows\*]キー状態の取得

タイプ
:   [Systemクラス](class_System)のメソッド

構文
:   getKeyState(code)

引数
:   |  |  |
    | --- | --- |
    | code | 状態を取得する仮想キーコード を指定します。 |

戻り値
:   キーが押されていれば真、押されていなければ偽になります。

説明
:   code で指定したキーコードに対応するキーが、このメソッドを呼んだ時点で押されているかどうかを取得します。
    Android場合常にfalseが返ります。