# BasicDrawDevice

Window.BasicDrawDevice クラスは、このインスタンスを Window.drawDevice に登録して使用するための DrawDevice で、標準的な描画機能を提供します。
Windows でのみ利用できます。
マルチプラットフォーム版では、非推奨となりました。
デフォルトで Canvas を使用した描画となり、DrawDevice はオプションで -graphicsystem=drawdevice を指定しなければ DrawDevice は使えません。
その場合 Canvas での描画は出来なくなります。

# メンバ

コンストラクタ
:   [BasicDrawDevice](func_BasicDrawDevice_BasicDrawDevice) ([Windows+]BasicDrawDevice オブジェクトの構築 )

メソッド
:   [recreate](func_BasicDrawDevice_recreate) ([Windows+]内部デバイス再生成 )

プロパティ
:   [interface](prop_BasicDrawDevice_interface) ([Windows+]インターフェースオブジェクトを取得 )

イベント
:   [onDisplayRotate](event_BasicDrawDevice_onDisplayRotate) ([Windows+]画面が回転されたとき )