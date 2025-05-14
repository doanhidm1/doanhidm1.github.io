# WaveSoundBuffer.labels

機能/意味
:   ラベル

タイプ
:   [WaveSoundBufferクラス](class_WaveSoundBuffer)のプロパティ

説明
:   ラベルを表すオブジェクトを得ることができます。
    このオブジェクトは辞書配列で、それぞれ、ループ情報中のラベルの名前をメンバ名とした要素が入っています。
    それぞれの要素も辞書配列で、name メンバはラベルの名前を表し、position メンバはミリ秒単位でのラベルの位置を表し、samplePosition はサンプル数単位でのラベルの位置を表しています。
    この辞書配列は読み出し専用であると考えてください。
    値を代入したり、新しいメンバを作成しても反映されることはありません。
    例:

    `var buf = new WaveSoundBuffer(window);
    (略)
    debug.message(buf.labels['start'].position);
    // 'start' というラベル名の位置をミリ秒単位で
    debug.message(buf.labels['start'].samplePosition);
    // 'start' というラベル名の位置をサンプル数単位で`