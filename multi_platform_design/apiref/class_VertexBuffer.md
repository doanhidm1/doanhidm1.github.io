# VertexBuffer

VertexBufferは頂点情報を保持するクラスです。

位置の指定やUV座標、頂点カラーなどを細かく設定したい場合に使用します。
単純な矩形ではなくメッシュ変形などを行いたい場合やポイントスプライトを使用したい場合などにも使用します。

プラグインで頂点の配列を直接変更できるようにポインタアクセスも可能です(ただしOpenGLES3.0以降)。
シェーダー+TJS2スクリプト+プラグインでの頂点操作で従来のようなLayer拡張性を確保できます。
従来のプラグイン内でほぼ完結していたものに比べるとやや複雑にはなります。

# メンバ

コンストラクタ
:   [VertexBuffer](func_VertexBuffer_VertexBuffer) (頂点配列を指定して頂点バッファを作ります )
    [VertexBuffer](func_VertexBuffer_VertexBuffer_1) (未初期化の頂点バッファを作ります )

メソッド
:   [lock](func_VertexBuffer_lock) (頂点データをロックし、データへのポインタ(read/write指定)を返します )
    [setVertex](func_VertexBuffer_setVertex) (頂点データを設定/更新 )
    [unlock](func_VertexBuffer_unlock) (頂点データのロックを解除します )

プロパティ
:   [dataType](prop_VertexBuffer_dataType) (頂点データの型(readonly) )
    [isIndex](prop_VertexBuffer_isIndex) (インデックスバッファかどうか(readonly) )
    [nativeHandle](prop_VertexBuffer_nativeHandle) (ネイティブハンドル )
    [size](prop_VertexBuffer_size) (バッファサイズ(readonly) )
    [updateType](prop_VertexBuffer_updateType) (データ更新頻度(readonly) )

イベント

定数
:   dtByte (データ型定数(byte) )
    dtFixed (データ型定数(fixed:固定少数点) )
    dtFloat (データ型定数(float) )
    dtInt (データ型定数(int) ES3.0以降必要 )
    dtShort (データ型定数(short) )
    dtUByte (データ型定数(unsigned byte) )
    dtUInt (データ型定数(unsinged int) ES3.0以降必要 )
    dtUShort (データ型定数(unsigned short) )
    ptLineLoop (プリミティブ型定数(ラインループ) )
    ptLines (プリミティブ型定数(ラインリスト) )
    ptLineStrip (プリミティブ型定数(ラインストリップ) )
    ptPoints (プリミティブ型定数(ポイントリスト) )
    ptTriangleFan (プリミティブ型定数(トライアングルファン) )
    ptTriangles (プリミティブ型定数(トライアングルリスト) )
    ptTriangleStrip (プリミティブ型定数(トライアングルストラップ) )
    utDynamic (更新頻度定数:頻繁に更新される )
    utStatic (更新頻度定数:変更なし )
    utStream (更新頻度定数:毎フレーム更新 )