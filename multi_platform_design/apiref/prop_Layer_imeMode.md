# Layer.imeMode

機能/意味
:   IMEモード

タイプ
:   [Layerクラス](class_Layer)のプロパティ

説明
:   IMEのモードを表します。値を設定することもできます。
    レイヤにフォーカスが設定されると、IMEはここで指定したモードに切り替わります。
    設定可能な値は以下の通りです。

    * imDisable を指定すると、IMEは無効になります。IMEを使用した入力はできませんし、ユーザの操作でもIMEを有効にすることはできません。
    * imClose を指定すると、IMEは無効になります。imDisableと異なり、ユーザの操作でIMEを有効にすることができます。
    * imOpen を指定すると、IMEは有効になります。
    * imDontCare を指定すると、IMEの有効/無効の状態は、前の状態を引き継ぎます。ユーザの操作によってIMEを有効にしたり無効にしたりすることができます。日本語入力においては、半角/全角文字をユーザに自由に入力させる場合の一般的なモードです。
    * imSAlpha を指定すると、IMEは有効になり、半角アルファベット入力モードになります。
    * imAlpha を指定すると、IMEは有効になり、全角アルファベット入力モードになります。
    * imHira を指定すると、IMEは有効になり、ひらがな入力モードになります。
    * imSKata を指定すると、IMEは有効になり、半角カタカナ入力モードになります。
    * imKata を指定すると、IMEは有効になり、全角カタカナ入力モードになります。
    * imChinese を指定すると、IMEは有効になり、2バイト中国語入力を受け付けるモードになります。日本語環境では使用できません。
    * imSHanguel を指定すると、IMEは有効になり、1バイト韓国語入力を受け付けるモードになります。日本語環境では使用できません。
    * imHanguel を指定すると、IMEは有効になり、2バイト韓国語入力を受け付けるモードになります。日本語環境では使用できません。

    未指定時は imDisable になります。

参照
:   [Window.imeMode](prop_Window_imeMode)