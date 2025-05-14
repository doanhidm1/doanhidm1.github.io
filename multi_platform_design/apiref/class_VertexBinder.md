# VertexBinder

VertexBinderはVertexBufferとシェーダーに入力する頂点情報を関連付けるためのクラスです。
ShaderProgramのプロパティにはこのクラスのインスタンスを設定します。
ShaderProgramに設定されたVertexBinderは、Canvs.drawMeshで呼び出された時シェーダーへ頂点情報として渡されます。

# メンバ

コンストラクタ
:   [VertexBinder](func_VertexBinder_VertexBinder) (コンストラクタ )

メソッド

プロパティ
:   [componentCount](prop_VertexBinder_componentCount) (頂点要素数 (1～4) )
    [normalize](prop_VertexBinder_normalize) (正規化するかどうか )
    [offset](prop_VertexBinder_offset) (頂点バッファオフセット(バイト数) )
    [stride](prop_VertexBinder_stride) (頂点ごとのストライド(バイト数) )
    [vertexBuffer](prop_VertexBinder_vertexBuffer) (頂点バッファ(VertexBufferクラス readonly) )

イベント