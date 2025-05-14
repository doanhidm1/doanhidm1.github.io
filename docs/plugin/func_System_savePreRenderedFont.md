# System.savePreRenderedFont

機能/意味
:   レンダリング済みフォントデータをファイルに保存する

タイプ
:   [Systemクラス](class_System)のメソッド

構文
:   savePreRenderedFont(storage, characters, callback)

引数
:   |  |  |
    | --- | --- |
    | storage | 保存するファイル名 |
    | characters | 保存する文字（キャラクタコード）の入った配列 |
    | callback | 情報とイメージを取得するコールバック キャラクタコードを引数に取り，レイヤ(PreRenderedFontImage)を返す関数であること function(ch) { return layer; } |

戻り値
:   なし (void)

説明