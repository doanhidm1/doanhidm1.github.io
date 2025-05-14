# Clipboard.setMultipleData

機能/意味
:   クリップボードに複数形式のデータを一括登録する

タイプ
:   [Clipboardクラス](class_Clipboard)のメソッド

構文
:   setMultipleData(data)

引数
:   |  |  |
    | --- | --- |
    | data | データを辞書形式で指定する。 |

戻り値
:   なし (void)

説明
:   データは複数の「データ形式:データ本体」の対を辞書で指定する。
    対応しているデータは以下の通り
    - text: テキストデータ
    - tjs: TJS式
    - bitmap: レイヤ