# KAGParser

KAGParser クラスは、KAG のシナリオを解析するためのクラスです。

# メンバ

コンストラクタ
:   [KAGParser](f_KAGParser_KAGParser)

メソッド
:   [assign](f_KAGParser_assign) ( KAGParser オブジェクトのコピー )
    [callLabel](f_KAGParser_callLabel) ( 現在位置をスタックに積んでの、指定ラベルへの移動 )
    [clear](f_KAGParser_clear) ( オブジェクトのクリア )
    [clearCallStack](f_KAGParser_clearCallStack) ( call タグ呼び出しスタックのクリア )
    [getNextTag](f_KAGParser_getNextTag) ( 次のタグを得る )
    [goToLabel](f_KAGParser_goToLabel) ( 指定ラベルへの移動 )
    [interrupt](f_KAGParser_interrupt) ( interrupted 状態にする )
    [loadScenario](f_KAGParser_loadScenario) ( シナリオの読み込み )
    [resetInterrupt](f_KAGParser_resetInterrupt) ( interrupted 状態の解除 )
    [restore](f_KAGParser_restore) ( 辞書配列からオブジェクトの状態を復元する )
    [store](f_KAGParser_store) ( オブジェクトの状態を辞書配列に書き出す )

プロパティ
:   [callStackDepth](f_KAGParser_callStackDepth) ( call タグ呼び出しスタックの深さ )
    [curLabel](f_KAGParser_curLabel) ( 現在のラベル )
    [curLine](f_KAGParser_curLine) ( 現在行の行数 )
    [curLineStr](f_KAGParser_curLineStr) ( 現在行の文字列 )
    [curPos](f_KAGParser_curPos) ( 現在行における文字の位置 )
    [curStorage](f_KAGParser_curStorage) ( 現在のストレージ )
    [debugLevel](f_KAGParser_debugLevel) ( デバッグレベル )
    [ignoreCR](f_KAGParser_ignoreCR) ( 改行を無視するかどうか )
    [macroParams](f_KAGParser_macroParams) ( 現在実行されているマクロの引数 )
    [macros](f_KAGParser_macros) ( マクロの入った辞書配列 )
    [processSpecialTags](f_KAGParser_processSpecialTags) ( 特殊タグを処理するかどうか )

イベント
:   [onAfterReturn](f_KAGParser_onAfterReturn) ( return タグで復帰した )
    [onCall](f_KAGParser_onCall) ( call タグが呼ばれた )
    [onJump](f_KAGParser_onJump) ( jump タグが呼ばれた )
    [onLabel](f_KAGParser_onLabel) ( ラベルを通過した )
    [onReturn](f_KAGParser_onReturn) ( return タグが呼ばれた )
    [onScenarioLoad](f_KAGParser_onScenarioLoad) ( シナリオ読み込みが開始した )
    [onScenarioLoaded](f_KAGParser_onScenarioLoaded) ( シナリオ読み込みが終了した )
    [onScript](f_KAGParser_onScript) ( iscript ブロックを通過した )