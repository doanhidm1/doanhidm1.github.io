# WIN32Dialog.insertTab

機能/意味
:   タブコントロールを利用する.

タイプ
:   [WIN32Dialogクラス](class_WIN32Dialog)のメソッド

構文
:   insertTab(tab\_id, pos, label)

引数

戻り値
:   なし (void)

説明
:   利用手順を検討中
    insertTab(IDC\_TAB, 0, "基本"); // タブを追加
    // deleteTab(IDC\_TAB, 0); // タブを削除
    // deleteAllTab(IDC\_TAB); // タブをすべて削除
    var dlg = new WIN32Dialog(); dlg.loadResource("resource.dll", "INNER"); // Border=None, Style=Child にしたダイアログ
    selectTab(IDC\_TAB, dlg); // 表示
    insertTab(IDC\_TAB, 1, "拡張");
    var dlg2 = new WIN32Dialog(); dlg2.loadResource("resource.dll", "INNER2");
    dlg.show(SW\_HIDE);
    selectTab(IDC\_TAB, dlg2); // 切り替え
    // onNotify で notify->code == TCN\_SELCHANGE かつ notify->idFrom == IDC\_TAB の場合にユーザーによるタブの切り替え
    // getCurSel(tab\_id) でタブの番号を取得し、対応するダイアログを SW\_SHOW、それ以外を SW\_HIDE する
    // タブ番号と対応するダイアログは自分で管理すること
    ※ dlg,dlg2 の open は selectTab されたときに行われるので、show(SW\_HIDE) するときは isValid で open されているか確認のこと