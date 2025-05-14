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
    Ctrlキーと同時に押された場合は、以下に示すようなコントロールコードが送られてきます。
    0x00 : Ctrl+@
    0x01 : Ctrl+A
    0x02 : Ctrl+B
    0x03 : Ctrl+C
    0x04 : Ctrl+D
    0x05 : Ctrl+E
    0x06 : Ctrl+F
    0x07 : Ctrl+G
    0x08 : Ctrl+H
    0x09 : Ctrl+I
    0x0A : Ctrl+J
    0x0B : Ctrl+K
    0x0C : Ctrl+L
    0x0D : Ctrl+M
    0x0E : Ctrl+N
    0x0F : Ctrl+O
    0x10 : Ctrl+P
    0x11 : Ctrl+Q
    0x12 : Ctrl+R
    0x13 : Ctrl+S
    0x14 : Ctrl+T
    0x15 : Ctrl+U
    0x16 : Ctrl+V
    0x17 : Ctrl+W
    0x18 : Ctrl+X
    0x19 : Ctrl+Y
    0x1A : Ctrl+Z
    0x1B : Ctrl+[
    0x1C : Ctrl+\
    0x1D : Ctrl+]
    0x1E : Ctrl+^
    0x1F : Ctrl+\_