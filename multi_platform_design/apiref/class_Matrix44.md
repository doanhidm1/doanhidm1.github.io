# Matrix44

4x4行列です。
OpenGLのため列優先行列であることに注意してください(列優先の方が演算量的に有利です)。
DirectXなどから見ると転置されているように感じます(シェーダのHLSLでは列優先で同じです)。

# メンバ

メソッド
:   [add](func_Matrix44_add) (自身に行列を加算します )
    [div](func_Matrix44_div) (自身から行列を除算します )
    [frustum](func_Matrix44_frustum) (透視投影変換行列を設定 )
    [mul](func_Matrix44_mul) (自身に行列を乗算します )
    [ortho](func_Matrix44_ortho) (平行投影変換行列を設定 )
    [ortho](func_Matrix44_ortho_1) (平行投影変換行列を設定 )
    [perspective](func_Matrix44_perspective) (射影変換行列を設定 )
    [perspectiveFov](func_Matrix44_perspectiveFov) (射影変換行列を設定 )
    [project](func_Matrix44_project) (各種行列を用いた座標変換 )
    [reset](func_Matrix44_reset) (単位行列化 )
    [rotate](func_Matrix44_rotate) (行列を回転します )
    [scale](func_Matrix44_scale) (行列を拡大縮小します )
    [set](func_Matrix44_set) (マトリックス設定 )
    [set](func_Matrix44_set_1) (マトリックス設定 )
    [set](func_Matrix44_set_2) (マトリックス設定 )
    [setRotate](func_Matrix44_setRotate) (回転量設定 )
    [setRotateZ](func_Matrix44_setRotateZ) (回転量設定 )
    [setScale](func_Matrix44_setScale) (拡大率設定 )
    [setTranslate](func_Matrix44_setTranslate) (移動量設定 )
    [sub](func_Matrix44_sub) (自身から行列を減算します )
    [translate](func_Matrix44_translate) (行列を移動します )

プロパティ
:   [array](prop_Matrix44_array) (1次元配列で受け取る[r] )
    [m11](prop_Matrix44_m11) (m11 [1][1]位置の値 )
    [m12](prop_Matrix44_m12) (m12 [1][2]位置の値 )
    [m13](prop_Matrix44_m13) (m13 [1][3]位置の値 )
    [m14](prop_Matrix44_m14) (m14 [1][4]位置の値 )
    [m21](prop_Matrix44_m21) (m21 [2][1]位置の値 )
    [m22](prop_Matrix44_m22) (m22 [2][2]位置の値 )
    [m23](prop_Matrix44_m23) (m23 [2][3]位置の値 )
    [m24](prop_Matrix44_m24) (m24 [2][4]位置の値 )
    [m31](prop_Matrix44_m31) (m31 [3][1]位置の値 )
    [m32](prop_Matrix44_m32) (m32 [3][2]位置の値 )
    [m33](prop_Matrix44_m33) (m33 [3][3]位置の値 )
    [m34](prop_Matrix44_m34) (m34 [3][4]位置の値 )
    [m41](prop_Matrix44_m41) (m41 [4][1]位置の値 )
    [m42](prop_Matrix44_m42) (m42 [4][2]位置の値 )
    [m43](prop_Matrix44_m43) (m43 [4][3]位置の値 )
    [m44](prop_Matrix44_m44) (m44 [4][4]位置の値 )

イベント