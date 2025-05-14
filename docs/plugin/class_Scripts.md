# Scripts

Scripts クラスへの Javascript 機能拡張

# メンバ

メソッド
:   [callSQ](func_Scripts_callSQ) (Squirrel グローバルメソッドの呼び出し。 )
    [clone](func_Scripts_clone) (値のクローンを返す。 )
    [compareSQ](func_Scripts_compareSQ) (Squirrel用比較 )
    [compileSQ](func_Scripts_compileSQ) (Squirrel スクリプトのコンパイル処理 )
    [compileStorageSQ](func_Scripts_compileStorageSQ) (Squirrel スクリプトのファイルからのコンパイル処理 )
    [driveSQ](func_Scripts_driveSQ) (Squirrel疑似スレッド処理の稼働 )
    [enableDebugJS](func_Scripts_enableDebugJS) (デバッガの有効化 )
    [equalStruct](func_Scripts_equalStruct) (オブジェクト同士を比較する。辞書/配列の場合は中身の要素が再帰的に比較されます )
    [equalStructNumericLoose](func_Scripts_equalStructNumericLoose) (オブジェクト同士を比較する。辞書/配列の場合は中身の要素が再帰的に比較されます 数値がゆるく比較されます(0.0 と 0 を等しいとして扱います) )
    [evalJSON](func_Scripts_evalJSON) (JSON の文字列を解析して Array または Dictionary を返す )
    [evalJSONStorage](func_Scripts_evalJSONStorage) (JSON のファイルを解析して Array または Dictionary を返す )
    [execJS](func_Scripts_execJS) (Javascript スクリプトの実行。 )
    [execSQ](func_Scripts_execSQ) (Squirrel スクリプトの実行。 )
    [execStorageJS](func_Scripts_execStorageJS) (Javascript スクリプトのファイルからの実行。 )
    [execStorageSQ](func_Scripts_execStorageSQ) (Squirrel スクリプトのファイルからの実行。 )
    [execStorageWSH](func_Scripts_execStorageWSH) (WSH スクリプトのファイルからの実行 )
    [execWSH](func_Scripts_execWSH) (WSH スクリプトの実行 )
    [foreach](func_Scripts_foreach) (オブジェクトのメンバの全参照 )
    [forkSQ](func_Scripts_forkSQ) (Squirrel スクリプトのスレッド実行。 )
    [forkStorageSQ](func_Scripts_forkStorageSQ) (Squirrel スクリプトのファイルからのスレッド実行。 )
    [getMD5HashString](func_Scripts_getMD5HashString) (octet の MD5ハッシュ値の取得 )
    [getObjectContext](func_Scripts_getObjectContext) (オブジェクトのコンテキストを返す )
    [getObjectCount](func_Scripts_getObjectCount) (オブジェクトのメンバ個数を返す )
    [getObjectKeys](func_Scripts_getObjectKeys) (オブジェクトのメンバ名一覧を返す )
    [isNullContext](func_Scripts_isNullContext) (オブジェクトのコンテキスト判定 )
    [loadSQ](func_Scripts_loadSQ) (Squirrel スクリプトの読み込み )
    [loadStorageSQ](func_Scripts_loadStorageSQ) (Squirrel スクリプトの読み込み )
    [processDebugJS](func_Scripts_processDebugJS) (デバッガ処理駆動 )
    [registerSQ](func_Scripts_registerSQ) (Squirrel のグローバル空間に TJS2 のオブジェクト/関数を登録する )
    [rehash](func_Scripts_rehash) (TJSDoRehash()を呼ぶ )
    [saveJSON](func_Scripts_saveJSON) (データを JSON 形式で保存する )
    [saveSQ](func_Scripts_saveSQ) (データを Squirrel 形式で保存する。このファイルは "return" を先頭にもつので dofile() で読みだすことができます )
    [setEvalErrorLog](func_Scripts_setEvalErrorLog) (Scripts.evalのエラーログ出力抑制 )
    [toJSONString](func_Scripts_toJSONString) (データを JSON 形式の文字列に変換する )
    [toSQString](func_Scripts_toSQString) (データを Squirrel 形式の文字列に変換する )
    [triggerSQ](func_Scripts_triggerSQ) (Squirrel疑似スレッド用のトリガ呼び出し )
    [unregisterSQ](func_Scripts_unregisterSQ) (Squirrel のグローバル空間に登録されたオブジェクトを解放する )

プロパティ
:   [threadCountSQ](prop_Scripts_threadCountSQ) ( )