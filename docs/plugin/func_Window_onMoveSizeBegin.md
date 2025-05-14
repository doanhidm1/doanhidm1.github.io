# Window.onMoveSizeBegin

機能/意味
:   ■拡張イベント：リサイズ・移動開始通知/終了

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   onMoveSizeBegin()

引数

戻り値
:   なし (void)

説明
:   フレームやタイトルバーをドラッグ開始した時やAlt+SpaceでSやMを選んだ時（開始通知），
    および移動やリサイズが終了した時（終了通知）にそれぞれ呼ばれる
    onMovingやonResizing中に元のウィンドウ位置やサイズを参照したい時はここで保存しておくとよい
    リサイズか移動かは WM\_ENTERSIZEMOVE/WM\_EXITSIZEMOVE の都合で判定不可