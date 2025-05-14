# Font.rasterizer

機能/意味
:   文字列描画方式

タイプ
:   [Fontクラス](class_Font)のプロパティ

説明
:   文字列描画方式を表します。
    値を設定することもできます。
    値は以下のどちらかを指定します(Windows以外では常にFreeTypeです)。

    * frGDI : GDI を使って文字を描画します(Windows版のみ)
    * frFreeType : FreeType を使って文字を描画します

    FreeType を指定した場合、横書きにのみ対応しています。
    その他は未対応です。
    このプロパティはスタティックです。
    Font.rasterizer を用いて値を設定してください。
    マルチプラットフォーム版からデフォルトがFreeTypeになりました。