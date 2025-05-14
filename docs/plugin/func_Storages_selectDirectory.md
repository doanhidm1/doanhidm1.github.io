# Storages.selectDirectory

機能/意味
:   フォルダ選択ダイアログを開く

タイプ
:   [Storagesクラス](class_Storages)のメソッド

構文
:   selectDirectory(params, title, window, rootDir)

引数
:   |  |  |
    | --- | --- |
    | params | selectFile と同様のパラメータを設定する |

戻り値
:   フォルダを選択してOKボタンを押せば真、キャンセルボタンを押せば偽\nparams.name フォルダ名を指定します。OKボタンを押した場合、選択されたフォルダがこのメンバに設定されます\nparams.title ダイアログボックスのタイトルを表示します\nparams.window ダイアログを開くWindowオブジェクトを指定します(void なら mainWindow が、未指定ならデスクトップがオーナーウィンドウとなります。デスクトップがオーナーの場合は、モードレス)\nparams.rootDir フォルダ選択のルートを指定します(このフォルダ以下のみ表示されます)

説明