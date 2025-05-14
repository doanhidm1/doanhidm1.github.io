# WaveSoundBuffer.filters

機能/意味
:   フィルタ配列

タイプ
:   [WaveSoundBufferクラス](class_WaveSoundBuffer)のプロパティ

説明
:   インサーションフィルタオブジェクトを保持している配列(Arrayクラスのインスタンス)です。
    この配列にフィルタオブジェクトを登録することにより、再生中にリアルタイムで音声に対して様々な効果をかけることができます。
    フィルタ配列への変更が反映されるのは、WaveSoundBuffer.openメソッドが実行された時だけです。
    それまでは、この配列への変更を行っても反映はされません。
    例:
     `var buf = new WaveSoundBuffer(window);
    (略)
    buf.filters.clear();
    // フィルタ配列をクリア
    buf.filters.add(new WaveSoundBuffer.PhaseVocoder());
    // PhaseVocoderフィルタを追加
    buf.filters[0].time = 0.5;
    // 倍速再生`