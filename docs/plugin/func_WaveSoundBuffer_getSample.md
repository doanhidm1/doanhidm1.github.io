# WaveSoundBuffer.getSample

機能/意味
:   サンプル値の取得（旧方式）

タイプ
:   [WaveSoundBufferクラス](class_WaveSoundBuffer)のメソッド

構文
:   getSample(n)

引数
:   |  |  |
    | --- | --- |
    | n | 取得するサンプルの数。省略すると 100 |

戻り値
:   平均値\n※ 予めuseVisBuffer=trueにしておくこと

説明
:   現在の再生位置から指定数のサンプルを取得してその平均値を返します。
    値が負のサンプル値は無視されます。