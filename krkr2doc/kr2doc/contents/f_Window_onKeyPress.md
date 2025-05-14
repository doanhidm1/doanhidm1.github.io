# Window.onKeyPress

機能/意味
:   文字が入力された

タイプ
:   [Windowクラス](f_Window)のイベント

構文
:   onKeyPress(key)

引数
:   |  |  |
    | --- | --- |
    | key | 入力された文字です。 |

説明
:   文字が入力されたときに発生します。[Window.onKeyDown](f_Window_onKeyDown) と異なるのは、onKeyDown が
    仮想キーコードを扱うのに対し、このイベントは文字そのものを扱います。押されたキーが
    文字とは関係のないキー (ファンクションキーなど) の場合はこのイベントは発生しません。