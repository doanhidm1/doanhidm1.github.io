# 開発者編 FAQ

初めに

吉里吉里で開発中に遭遇する可能性のある問題についての FAQ です。

配布

Q.exeのアイコンを変更したい
:   A.吉里吉里Zでは標準のアイコン変更ツールは付属していません。
    Visual Studio でアイコンを変更して再ビルドするか、リソースを変更するフリーソフトでアイコンを変更してください。
    ["exe リソース 書き換え フリーソフト"](https://www.google.co.jp/?gws_rd=ssl#safe=off&q=exe+%E3%83%AA%E3%82%BD%E3%83%BC%E3%82%B9+%E6%9B%B8%E3%81%8D%E6%8F%9B%E3%81%88+%E3%83%95%E3%83%AA%E3%83%BC%E3%82%BD%E3%83%95%E3%83%88&pws=0) などで検索してください。

動画

Q.MPEG 1を使用して横 1024 を超えるとアスペクト比がおかしくなる
:   A.Mixer(VMR)やオーバーレイモードの場合アスペクト比がおかしくなる不具合が環境かkrmovieの実装にあるようです。
    レイヤーモードを使用するか WMV、H.264 を使用してください。

Q.WMV をオーバーレイモードで再生すると上下反転する
:   A.環境によって発生するようです。
    Mixer(VMR)モードを使用するようにしてください。

セーブデータ

Q.スクリプトを修正してもその変更が反映されない
:   A.savedate フォルダに修正前のセーブデータが残っていて、そのデータによって挙動がおかしくなっている可能性があります。
    savedate フォルダを丸々消してから再実行すると解消されるかもしれません。

各種ツール

Q.付属のツールなど、吉里吉里で使うデータ以外の用途で使ってもいいの？
:   A.付属ツールの使い道には特に制限などありません。