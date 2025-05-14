# サウンドシステムについて

吉里吉里のサウンドシステムは MIDI、CD-DA、Wave (PCM) を再生できます。
　MIDI 再生はシーケンサを内蔵しており、再生チャンネルが重ならなければ同時再生できます。
　CD-DA 再生は再生ドライブが重ならなければ同時再生でき、CD-ROM ドライブそれ自体に対して音量を制御することもできます。
　Wave 再生は複数を同時再生でき、ストリーミング再生 (長いサウンドを少しずつ読み込みながら再生) をすることができるほか、サウンドループ情報ファイル (.sli ファイル) を用いて、つぎめを感じさせないシームレスなループ再生を実現できます (サウンドループ情報ファイルはループチューナで作成します)。

# WaveSoundBuffer で再生可能な形式

[WaveSoundBuffer](f_WaveSoundBuffer) では、標準で無圧縮の RIFF Wave 形式 ( 拡張は .wav で、Windows 標準形式 ) を再生することができます。受け付けられる形式は以下の通りです。

* WAVE\_FORMAT\_PCM 形式で、8bit 以上 32bit 以下の整数 PCM、かつチャンネル数が 1(モノラル)、2(ステレオ), 4(quadraphonic)、6(5.1ch) のもの
* WAVE\_FORMAT\_IEEE\_FLOAT 形式で、32bit の浮動小数点数 PCM、かつチャンネル数が 1(モノラル)、2(ステレオ), 4(quadraphonic)、6(5.1ch) のもの
* WAVE\_FORMAT\_EXTENSIBLE 形式で、サブタイプが KSDATAFORMAT\_SUBTYPE\_PCM 形式で8bit 以上 32bit 以下の整数 PCM
* WAVE\_FORMAT\_EXTENSIBLE 形式で、サブタイプが KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT 形式の 32bit 浮動小数点数 PCM

　16bit を越える整数 PCM (24bit PCM など) や 浮動小数点数 PCM、ステレオを越えるチャンネル数のサウンド ( 4chサウンドや5.1chサウンドなど ) の再生は、WDM 系のサウンドドライバを使用しているシステム ( Windows2000, XP 以降、 Windows 98/98SE/ME で WDM ドライバ使用のシステム ) でのみのサポートとなります。

　また、WaveSoundBuffer で再生可能な形式は、プラグインによって拡張することができます。

# WaveSoundBuffer での 4ch および 6ch の扱い

WAVE\_FORMAT\_EXTENSIBLE は、データ内に「どのチャンネルがどのスピーカーに割り当てられているか」の情報を持っていますが、WAVE\_FORMAT\_PCM や WAVE\_FORMAT\_IEEE\_FLOAT の場合はその情報を持っていません。吉里吉里が WAVE\_FORMAT\_PCM や WAVE\_FORMAT\_IEEE\_FLOAT で 4ch や 6ch のデータを扱うときは次のように解釈します。

4chのとき
:   チャンネルの先頭から、それぞれ、前左、前右、後左、後右のスピーカー用データであると見なされます

6chのとき
:   チャンネルの先頭から、それぞれ、前左、前中央、前右、後左、後右、低周波のスピーカー用データであると見なされます

また、OggVorbis で 4ch や 6ch のサウンドを再生するときにもこれと同じルールが適用されます。