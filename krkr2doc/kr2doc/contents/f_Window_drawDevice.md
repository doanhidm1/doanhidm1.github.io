# Window.drawDevice

機能/意味
:   描画デバイス

タイプ
:   [Windowクラス](f_Window)のプロパティ (読み書き可能)

説明
:   描画デバイスオブジェクトを表します。
    　値を設定することもできます。値を設定すると、以前このウィンドウに指定されていた描画デバイスは自動的に
    無効になります (invalidateされます)。
    　デフォルトでは、Window.PassThroughDrawDevice というクラスのインスタンスが指定されています。
    　Window.PassThroughDrawDevice の詳細については、吉里吉里ソースの core/visual/win32/PassThroughDrawDevice.cpp 内の説明も参照してください。
    　独自の描画デバイス (プラグインで提供される物) を指定する場合は、そのプラグインのドキュメントに
    従ってください。