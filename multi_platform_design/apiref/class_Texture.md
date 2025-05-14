# Texture

テクスチャクラス。
ハードウェア上のテクスチャとほぼ対応しています。

invalidateすることでテクスチャは無効化されるため、必要なくなったら明示的にinvalidate呼び出すことを推奨します。

# メンバ

コンストラクタ
:   [Texture](func_Texture_Texture) (ファイル読み込み版コンストラクタ )
    [Texture](func_Texture_Texture_1) (ミップマップ生成版コンストラクタ )
    [Texture](func_Texture_Texture_2) (サイズ指定版コンストラクタ )
    [Texture](func_Texture_Texture_3) (Bitmapコピー版コンストラクタ )

メソッド
:   [copyRect](func_Texture_copyRect) (矩形コピー(位置指定Rect版) )
    [copyRect](func_Texture_copyRect_1) (矩形コピー(位置指定) )
    [copyRect](func_Texture_copyRect_2) (矩形コピー(全コピー) )
    [setDrawSize](func_Texture_setDrawSize) (描画基準サイズの設定 )

プロパティ
:   [height](prop_Texture_height) (高さ(有効範囲) )
    [isGray](prop_Texture_isGray) (8bitカラーかどうか(内部ではアルファテクスチャ) )
    [isPowerOfTwo](prop_Texture_isPowerOfTwo) (テクスチャサイズが2の累乗値かどうか )
    [margin9Patch](prop_Texture_margin9Patch) (9patchマージン )
    [memoryHeight](prop_Texture_memoryHeight) (実際(ハードウェア上)の高さ )
    [memoryWidth](prop_Texture_memoryWidth) (実際(ハードウェア上)の幅 )
    [nativeHandle](prop_Texture_nativeHandle) (ネイティブハンドル(環境依存) )
    [stretchType](prop_Texture_stretchType) (拡大縮小時の補間方法 )
    [width](prop_Texture_width) (幅(有効範囲) )
    [wrapModeHorizontal](prop_Texture_wrapModeHorizontal) (水平方向ラップモード )
    [wrapModeVertical](prop_Texture_wrapModeVertical) (垂直方向ラップモード )

イベント

定数
:   stLinear (線形補間。stretchTypeプロパティに設定します。 )
    stNearest (最近傍点法。stretchTypeプロパティに設定します。 )
    wmClampToEdge (端色引き延ばし。wrapModeHorizontal/wrapModeVerticalプロパティに設定します。2の累乗サイズでない場合はこの定数でなければなりません(default)。 )
    wmMirror (ミラー繰り返し。wrapModeHorizontal/wrapModeVerticalプロパティに設定します。 )
    wmRepeat (繰り返し。wrapModeHorizontal/wrapModeVerticalプロパティに設定します。 )