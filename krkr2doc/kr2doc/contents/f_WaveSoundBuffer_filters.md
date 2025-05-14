# WaveSoundBuffer.filters

機能/意味
:   フィルタ配列

タイプ
:   [WaveSoundBufferクラス](f_WaveSoundBuffer)のプロパティ (読み出し専用)

説明
:   インサーションフィルタオブジェクトを保持している配列(Arrayクラスのインスタンス)です。
    　この配列にフィルタオブジェクトを登録することにより、再生中にリアルタイムで音声に対して
    様々な効果をかけることができます。
    　フィルタ配列への変更が反映されるのは、[WaveSoundBuffer.open](f_WaveSoundBuffer_open)メソッドが実行された
    時だけです。それまでは、この配列への変更を行っても反映はされません。
    `例:
    var buf = new WaveSoundBuffer(window);
    (略)
    buf.filters.clear(); // フィルタ配列をクリア
    buf.filters.add(new WaveSoundBuffer.PhaseVocoder()); // PhaseVocoderフィルタを追加
    buf.filters[0].time = 0.5; // 倍速再生`