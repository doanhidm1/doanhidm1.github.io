# VertexBinder.normalize

機能/意味
:   正規化するかどうか

タイプ
:   [VertexBinderクラス](class_VertexBinder)のプロパティ

説明
:   デフォルトはfalse。
    trueの場合、非float型の時[-1.0～0.0～1.0]の間に正規化されシェーダーに送られます。
    色情報などubyte形で0～255で色を指定し、その色を0.0～1.0に正規化してシェーダーで使う等するときに指定します。