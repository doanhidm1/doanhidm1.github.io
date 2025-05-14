# Window.drawDevice

機能/意味
:   [Windows+]描画デバイス

タイプ
:   [Windowクラス](class_Window)のプロパティ

説明
:   描画デバイスオブジェクトを表します。
    描画デバイスは非推奨になりました。
    Canvas を使用した描画を推奨します。
    値を設定することもできます。
    値を設定すると、以前このウィンドウに指定されていた描画デバイスは自動的に無効になります (invalidateされます)。
    デフォルトでは、Window.BasicDrawDevice というクラスのインスタンスが指定されています。
    Window.BasicDrawDevice の詳細については、吉里吉里ソースの core/visual/win32/BasicDrawDevice.cpp 内の説明も参照してください。
    独自の描画デバイス (プラグインで提供される物) を指定する場合は、そのプラグインのドキュメントに従ってください。