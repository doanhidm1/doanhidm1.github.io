# BinaryStream

# メンバ

コンストラクタ
:   [BinaryStream](func_BinaryStream_BinaryStream)

メソッド
:   [close](func_BinaryStream_close) (オープン中のストレージを閉じる )
    [compress](func_BinaryStream_compress) (別のストレージからデータを圧縮しつつコピー )
    [copy](func_BinaryStream_copy) (別のストレージからデータをコピー )
    [decompress](func_BinaryStream_decompress) (別のストレージからデータを展開しつつコピー )
    [finalize](func_BinaryStream_finalize) ( )
    [open](func_BinaryStream_open) (ストレージを開く )
    [read](func_BinaryStream_read) (指定バイト読み込む )
    [readI16BE](func_BinaryStream_readI16BE) (2byte 読み込み (Big Endian) )
    [readI16LE](func_BinaryStream_readI16LE) (2byte 読み込み (Little Endian) )
    [readI32BE](func_BinaryStream_readI32BE) (4byte 読み込み (Big Endian) )
    [readI32LE](func_BinaryStream_readI32LE) (4byte 読み込み (Little Endian) )
    [readI64BE](func_BinaryStream_readI64BE) (8byte 読み込み (Big Endian) )
    [readI64LE](func_BinaryStream_readI64LE) (8byte 読み込み (Little Endian) )
    [readI8](func_BinaryStream_readI8) ({1,2,4,8}バイトを数値として読み込む )
    [seek](func_BinaryStream_seek) (ストリームのポジションを変更する )
    [setFilter](func_BinaryStream_setFilter) (フィルタDLLを設定する )
    [setProgressCallback](func_BinaryStream_setProgressCallback) (プログレスコールバックを設定する )
    [tell](func_BinaryStream_tell) (ストリームの現在のポジションを取得する )
    [write](func_BinaryStream_write) (データを書き込む )
    [writeI16BE](func_BinaryStream_writeI16BE) (2byte 書き込み (Big Endian) )
    [writeI16LE](func_BinaryStream_writeI16LE) (2byte 書き込み (Little Endian) )
    [writeI32BE](func_BinaryStream_writeI32BE) (4byte 書き込み (Big Endian) )
    [writeI32LE](func_BinaryStream_writeI32LE) (4byte 書き込み (Little Endian) )
    [writeI64BE](func_BinaryStream_writeI64BE) (8byte 書き込み (Big Endian) )
    [writeI64LE](func_BinaryStream_writeI64LE) (8byte 書き込み (Little Endian) )
    [writeI8](func_BinaryStream_writeI8) ({1,2,4,8}バイトで数値を書き込む )

プロパティ
:   [mode](prop_BinaryStream_mode) (現在のモード )
    [storage](prop_BinaryStream_storage) (現在開いているストレージ )

定数
:   bsAppend (追記 )
    bsRead (読み込み )
    bsSeekCur (現在位置から )
    bsSeekEnd (末尾から )
    bsSeekSet (先頭から )
    bsUpdate (更新 )
    bsWrite (書き込み )