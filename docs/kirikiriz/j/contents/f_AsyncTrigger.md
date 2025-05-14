# AsyncTrigger

AsyncTrigger クラスは、いったん吉里吉里に制御が戻った直後のイベント配信のタイミングにイベントを発生させるためのクラスです。この機能を非同期トリガ ( asynchronous trigger ) と呼びます。
　吉里吉里のようにイベント駆動型のプログラミングモデルをとるスクリプトにおいて、イベントハンドラ内では実行できないような処理 ( たとえばイベントの発生元のオブジェクトをそのイベントハンドラ内で無効化しようとするなど ) を、そのイベントハンドラ外で行いたい時に便利です。

# メンバ

コンストラクタ
:   [AsyncTrigger](f_AsyncTrigger_AsyncTrigger)

メソッド
:   [cancel](f_AsyncTrigger_cancel) ( トリガのキャンセル )
    [trigger](f_AsyncTrigger_trigger) ( トリガを引く )

プロパティ
:   [cached](f_AsyncTrigger_cached) ( イベントをキャッシュするかどうか )
    [mode](f_AsyncTrigger_mode) ( モード )

イベント
:   [onFire](f_AsyncTrigger_onFire) ( 発砲するとき )