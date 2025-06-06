# WIN32Dialog

Windows ネイティブダイアログを操作するためのクラスです。
APIのラッパ程度の機能しかないので非常に使いにくいですが，
後述のtjsで記述された WIN32DialogEX を使うと幸せになれます。

# メンバ

コンストラクタ
:   [WIN32Dialog](func_WIN32Dialog_WIN32Dialog)

メソッド
:   [chooseColor](func_WIN32Dialog_chooseColor) (static )
    [close](func_WIN32Dialog_close) (ダイアログを閉じる )
    [closeProgress](func_WIN32Dialog_closeProgress) (プログレスダイアログを閉じる )
    [deleteAllTab](func_WIN32Dialog_deleteAllTab) ( )
    [deleteTab](func_WIN32Dialog_deleteTab) ( )
    [getBaseUnits](func_WIN32Dialog_getBaseUnits) (GetDialogBaseUnit のラッパー )
    [getCurSel](func_WIN32Dialog_getCurSel) ( )
    [getItem](func_WIN32Dialog_getItem) (GetDlgItem のラッパー )
    [getItemClassName](func_WIN32Dialog_getItemClassName) (GetClassName のラッパー )
    [getItemEnabled](func_WIN32Dialog_getItemEnabled) ( )
    [getItemHeight](func_WIN32Dialog_getItemHeight) ( )
    [getItemID](func_WIN32Dialog_getItemID) (GetDlgCtrlID のラッパー )
    [getItemInt](func_WIN32Dialog_getItemInt) ( )
    [getItemLeft](func_WIN32Dialog_getItemLeft) ( )
    [getItemText](func_WIN32Dialog_getItemText) ( )
    [getItemTop](func_WIN32Dialog_getItemTop) ( )
    [getItemWidth](func_WIN32Dialog_getItemWidth) ( )
    [getScrollInfo](func_WIN32Dialog_getScrollInfo) (ScrollInfo の取得 )
    [InitCommonControls](func_WIN32Dialog_InitCommonControls) (InitCommonControls, InitCommonControlsEx のラッパー )
    [InitCommonControlsEx](func_WIN32Dialog_InitCommonControlsEx) ( )
    [insertTab](func_WIN32Dialog_insertTab) (タブコントロールを利用する. )
    [invalidateRect](func_WIN32Dialog_invalidateRect) (InvalidateRect のラッパー )
    [loadResource](func_WIN32Dialog_loadResource) (ダイアログリソースを読み込む )
    [makeTemplate](func_WIN32Dialog_makeTemplate) (ダイアログテンプレートを生成する )
    [mapRect](func_WIN32Dialog_mapRect) (MapDialogRect のラッパー )
    [messageBox](func_WIN32Dialog_messageBox) (static )
    [onCommand](func_WIN32Dialog_onCommand) (WM\_COMMAND のコールバック )
    [onHScroll](func_WIN32Dialog_onHScroll) (WM\_HSCROLL のコールバック )
    [onInit](func_WIN32Dialog_onInit) (WM\_INITDIALOG のコールバック )
    [onKeyDown](func_WIN32Dialog_onKeyDown) (WM\_KEYDOWN のコールバック )
    [onKeyUp](func_WIN32Dialog_onKeyUp) (WM\_KEYUP のコールバック )
    [onNotify](func_WIN32Dialog_onNotify) (WM\_NOTIFY のコールバック )
    [onVScroll](func_WIN32Dialog_onVScroll) (WM\_VSCROLL のコールバック )
    [open](func_WIN32Dialog_open) (ダイアログを開く )
    [openProgress](func_WIN32Dialog_openProgress) (プログレスダイアログを表示する )
    [openPropertySheet](func_WIN32Dialog_openPropertySheet) (static )
    [propSheetMessage](func_WIN32Dialog_propSheetMessage) (PSM\_\* メッセージをプロパティシートウィンドウに送信する )
    [selectTab](func_WIN32Dialog_selectTab) ( )
    [sendItemMessage](func_WIN32Dialog_sendItemMessage) (SendDlgItemMessage のラッパー )
    [setItemBitmap](func_WIN32Dialog_setItemBitmap) (アイテムにBitmapを設定する )
    [setItemEnabled](func_WIN32Dialog_setItemEnabled) (アイテムの有効・無効を設定・取得する )
    [setItemFocus](func_WIN32Dialog_setItemFocus) (アイテムにフォーカスを設定する )
    [setItemInt](func_WIN32Dialog_setItemInt) (Get/SetDlgItemInt/Text のラッパー )
    [setItemPos](func_WIN32Dialog_setItemPos) (アイテムの位置・大きさを変更・取得する )
    [setItemSize](func_WIN32Dialog_setItemSize) ( )
    [setItemText](func_WIN32Dialog_setItemText) ( )
    [setMessageResult](func_WIN32Dialog_setMessageResult) (DWL\_MSGRESULTの値を設定する )
    [setPos](func_WIN32Dialog_setPos) (ダイアログ座標を設定 )
    [setScrollInfo](func_WIN32Dialog_setScrollInfo) (ScrollInfo の設定 )
    [setSize](func_WIN32Dialog_setSize) (ダイアログの大きさを設定 )
    [show](func_WIN32Dialog_show) (ShowWindow のラッパー )

プロパティ
:   [height](prop_WIN32Dialog_height) ( )
    [HWND](prop_WIN32Dialog_HWND) (ダイアログのウィンドウハンドル )
    [icon](prop_WIN32Dialog_icon) (ダイアログのアイコン画像 )
    [isValid](prop_WIN32Dialog_isValid) (ダイアログを open しているかどうか )
    [left](prop_WIN32Dialog_left) (ダイアログサイズの取得 )
    [modeless](prop_WIN32Dialog_modeless) (モードレスダイアログ用のフラグ )
    [progress](prop_WIN32Dialog_progress) (プログレス状態かどうか )
    [progressCanceled](prop_WIN32Dialog_progressCanceled) (プログレスがキャンセルされたかどうか（※対象ボタンはIDCANCEL固定） )
    [progressValue](prop_WIN32Dialog_progressValue) (プログレスバーを更新する（0-100の数値 or 負数の場合マーキー状態の速度） )
    [propsheet](prop_WIN32Dialog_propsheet) (プロパティシートとして表示中かどうか )
    [top](prop_WIN32Dialog_top) ( )
    [width](prop_WIN32Dialog_width) ( )

定数
:   BM\_ (Button Control Messages )
    BN\_ (User Button Notification Codes )
    BS\_ (Button Control Styles )
    CB\_ (Combo Box messages )
    CB\_ (Combo Box return Values )
    CBN\_ (Combo Box Notification Codes )
    CBS\_ (Combo Box styles )
    DLG\_ (Dialog Codes )
    DM\_ (Dialog Control Messages )
    DS\_ (Dialog Styles )
    EC\_ (Edit control EM\_SETMARGIN parameters )
    EM\_ (Edit Control Messages )
    EN\_ (Edit Control Notification Codes )
    ES\_ (Edit Control Styles )
    FW\_ (Font Weights )
    ICC\_ (InitCommonControlsEx parameters )
    ID (Dialog Box Command IDs )
    LB\_ (Listbox Return Values )
    LBN\_ (Listbox Notification Codes )
    LBS\_ (Listbox Styles )
    MB\_ (MessageBox arguments )
    PSM\_ ( )
    PSN\_ (PropertySheet notifications/messages )
    SB\_ (Scroll bar option )
    SBM\_ (Scroll bar messages )
    SBS\_ (Scroll Bar Styles )
    SIF\_ ( )
    SS\_ (Static Control Constants )
    STM\_ (Static Control Mesages )
    SW\_ (ShowWindow options )
    TCN\_ (TabControl messages )
    WB\_ (EDITWORDBREAKPROC code values )
    WS\_ (Window Styles )
    WS\_EX\_ ( )