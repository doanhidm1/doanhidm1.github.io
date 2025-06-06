# if ステートメント

if ステートメントは、「○○ならば●●をする」というような、条件判断によってスクリプトの一部を実行するかしないかを決定させる構文です。
　構文は以下の通りです。

`if(expression)
    ステートメントまたはブロック
else
    ステートメントまたはブロック`

　最初の「ステートメントまたはブロック」は、expression を評価した結果が真の時に実行されるもので、２番目の「ステートメントまたはブロック」は、評価した結果が偽のときに実行されるものです。else 以降は必要ない場合は書かなくてかまいません。

`例:
    if(a==b)
        inform("a と b は同じです");

    if(a<b)
    {
        var t;
        t=a; a=b; b=t; // a と b を入れ替える
    }

    if(a==b)
        inform("a と b は同じです");
    else
        inform("a と b は違います");`

# if と else の対応

else は、「前の、まだ else と対応していない if に対応する」という規則を持っています。

たとえば、

`if(expr) // ★
        if(expr) // ●
            statement;
        else // ●
            statement;
    else // ★
        statement;`

　と記述した場合、★の else は ★ の if に、● の else は ● の if に対応することになります。
　TJS2のようなフリースタイルの言語は、たとえインデントを間違って

`if(expr) // ★
        if(expr) // ●
            statement;
    else // ●
        statement;`

　と書いても、対応は上記の通りですので注意する必要があります。
　対応をはっきり区切りたい場合は、

`if(expr) { // ★
        if(expr) // ●
            statement;
    }
    else // ★
        statement;`

　のようにブロックで囲むという方法を採ってください。