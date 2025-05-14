# VertexBuffer.unlock

機能/意味
:   頂点データのロックを解除します

タイプ
:   [VertexBufferクラス](class_VertexBuffer)のメソッド

構文
:   unlock()

引数

戻り値
:   なし (void)

説明
:   プラグイン用( OpenGL ES 3.0以降でないと使えません )。
    データの受け渡しが終わったら、バッファが使用される前に呼び出します。
    lockを維持せず、更新したら即座にunlockするのが好ましいです。