# System.externalStorageState

機能/意味
:   [Android+]外部ストレージの状態[r]

タイプ
:   [Systemクラス](class_System)のプロパティ

説明
:   Environment.getExternalStorageState()で取得されるもの。
    以下のいずれか

    * "unknown" 不明な状態
    * "removed" 取り外されている状態
    * "unmounted" マウントされていない状態
    * "checking" ディスクチェック中
    * "nofs" 未フォーマットかサポートされていないファイルシステム
    * "mounted" マウントされていて読み書き可能
    * "mounted\_ro" 読み取り専用でマウントされている
    * "shared" マウントされていない、USBマスストレージなど
    * "bad\_removal" アンマウントされる前に取り外された
    * "unmountable" マウントできない