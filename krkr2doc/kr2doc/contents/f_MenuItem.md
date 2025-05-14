# MenuItem

MenuItem クラスは、メニュー項目を管理するためのクラスです。
　ウィンドウのメニューバーにメニュー項目を並べたい場合は、[Window.menu](f_Window_menu) プロパティの
子としてメニュー項目を追加します。

# メンバ

コンストラクタ
:   [MenuItem](f_MenuItem_MenuItem)

メソッド
:   [add](f_MenuItem_add) ( 子メニュー項目の追加 )
    [insert](f_MenuItem_insert) ( 子メニュー項目の挿入 )
    [popup](f_MenuItem_popup) ( メニュー項目のポップアップ表示 )
    [remove](f_MenuItem_remove) ( 子メニュー項目の削除 )

プロパティ
:   [HMENU](f_MenuItem_HMENU) ( HMENUメニュー項目ハンドル )
    [caption](f_MenuItem_caption) ( キャプション )
    [checked](f_MenuItem_checked) ( チェックマークを表示するかどうか )
    [children](f_MenuItem_children) ( 子メニュー項目 )
    [enabled](f_MenuItem_enabled) ( 選択可能かどうか )
    [group](f_MenuItem_group) ( グループ番号 )
    [index](f_MenuItem_index) ( 順番 )
    [parent](f_MenuItem_parent) ( 親メニュー項目 )
    [radio](f_MenuItem_radio) ( ラジオ項目かどうか )
    [root](f_MenuItem_root) ( ルートメニュー項目 )
    [shortcut](f_MenuItem_shortcut) ( ショートカットキー )
    [visible](f_MenuItem_visible) ( 可視かどうか )
    [window](f_MenuItem_window) ( オーナーウィンドウ )

イベント
:   [onClick](f_MenuItem_onClick) ( メニュー項目が選択された )