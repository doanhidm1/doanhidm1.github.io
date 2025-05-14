# WaveSoundBuffer.globalFocusMode

機能/意味
:   フォーカスモード

タイプ
:   [WaveSoundBufferクラス](class_WaveSoundBuffer)のプロパティ

説明
:   フォーカスモードを表します。
    値を設定することもできます。
    フォーカスモードは、アプリケーションが最小化したときや非アクティブになったときにミュートするモードです。

    * sgfmNeverMuteを指定すると、アプリケーションがどのような状態でもミュートはしません。
    * sgfmMuteOnMinimizeを指定すると、アプリケーションが最小化時にミュートします。
    * sgfmMuteOnDeactivateを指定すると、アプリケーションが非アクティブ化したときにミュートします。

    このプロパティは WaveSoundBuffer クラス上にしか存在しません (WaveSoundBufferから作られたオブジェクト上にこのプロパティはありません)。
    使用する際は WaveSoundBuffer.globalFocusMode としてください。
    このプロパティの設定よりも、コマンドラインオプションで指定した '-wsmute' (DirectSound ミュート) の設定が優先されます。
    Androidでは、非アクティブになった時ミュートされます。
    バックグラウンドでは処理速度が低下し、正常に再生できなくなります。