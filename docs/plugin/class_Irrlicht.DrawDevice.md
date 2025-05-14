# DrawDevice

# メンバ

コンストラクタ
:   [DrawDevice](func_DrawDevice_DrawDevice)

メソッド
:   [getVisible](func_DrawDevice_getVisible) (プライマリレイヤの表示状態の指定 )
    [setSize](func_DrawDevice_setSize) (バックバッファのサイズ設定 )
    [setVisible](func_DrawDevice_setVisible) (プライマリレイヤの表示状態の指定 )

プロパティ
:   [defaultVisible](prop_DrawDevice_defaultVisible) (プライマリレイヤの標準の visible プライマリレイヤを生成時に表示するかどうかを指定します。 )
    [destHeight](prop_DrawDevice_destHeight) (< 実描画領域横幅(読み取り専用) )
    [destWidth](prop_DrawDevice_destWidth) ( )
    [height](prop_DrawDevice_height) (< バックバッファ横幅 )
    [interface](prop_DrawDevice_interface) ( )
    [width](prop_DrawDevice_width) ( )
    [zoomMode](prop_DrawDevice_zoomMode) (拡大モード: 初期値は true true: バックバッファから画面への転送時に拡大縮小します false: バックバッファのサイズを実際の画面上の解像度に追従させます false にした場合、Irrlicht 側の座標系がフルスクリーン化した時や、 Window.setZoom した時に変化するので注意が必要です。 )