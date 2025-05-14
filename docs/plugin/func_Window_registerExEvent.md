# Window.registerExEvent

機能/意味
:   拡張イベントを有効にする

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   registerExEvent()

引数

戻り値
:   なし (void)

説明
:   このウィンドウのインスタンスについて
    説明に「■拡張イベント：」と記述されているコールバックが有効になる

    ただし、下記のコールバックについては
    この関数を実行した時点でインスタンスに存在しない場合には発生しないので注意
    （ない場合は後からインスタンスに関数を追加しても呼ばれない）
    onMoving 移動中
    onMove 移動
    onResizing リサイズ中
    onNcMouseMove NonClient領域でのマウス移動