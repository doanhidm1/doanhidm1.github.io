# Matrix32

2次元用の3x2行列です。
OpenGLのため列優先行列であることに注意してください。

# メンバ

コンストラクタ
:   [Matrix32](func_Matrix32_Matrix32) (コンストラクタ(単位行列) )
    [Matrix32](func_Matrix32_Matrix32_1) (コンストラクタ )

メソッド
:   [multiply](func_Matrix32_multiply) (行列をかける(this = this \* matrix) )
    [premultiply](func_Matrix32_premultiply) (行列を後ろにかける(this = matrix \* this) )
    [preScale](func_Matrix32_preScale) (行列を拡大させる(事前拡大) )
    [reset](func_Matrix32_reset) (単位行列化 )
    [rotate](func_Matrix32_rotate) (行列を回転させる )
    [rotate](func_Matrix32_rotate_1) (行列を回転させる )
    [scale](func_Matrix32_scale) (行列を拡大させる )
    [set](func_Matrix32_set) (マトリックス設定 )
    [set](func_Matrix32_set_1) (マトリックス設定 )
    [set](func_Matrix32_set_2) (マトリックス設定 )
    [setRotate](func_Matrix32_setRotate) (回転行列を設定する )
    [setScale](func_Matrix32_setScale) (拡大行列を設定する )
    [setSkewX](func_Matrix32_setSkewX) (X軸傾斜行列を設定する )
    [setSkewY](func_Matrix32_setSkewY) (Y軸傾斜行列を設定する )
    [setTranslate](func_Matrix32_setTranslate) (移動行列を設定する )
    [skewX](func_Matrix32_skewX) (行列をX軸傾斜させる )
    [skewY](func_Matrix32_skewY) (行列をY軸傾斜させる )
    [transform](func_Matrix32_transform) (XY座標値をこの行列にかけ合わせて変換する )
    [translate](func_Matrix32_translate) (行列を移動させる )

プロパティ
:   [array](prop_Matrix32_array) (1次元配列で受け取る[r] )
    [m11](prop_Matrix32_m11) ([1][1]位置の値[r/w] )
    [m12](prop_Matrix32_m12) ([1][2]位置の値[r/w] )
    [m21](prop_Matrix32_m21) ([2][1]位置の値[r/w] )
    [m22](prop_Matrix32_m22) ([2][2]位置の値[r/w] )
    [m31](prop_Matrix32_m31) ([3][1]位置の値[r/w] )
    [m32](prop_Matrix32_m32) ([3][2]位置の値[r/w] )

イベント