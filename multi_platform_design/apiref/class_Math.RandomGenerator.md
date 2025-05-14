# RandomGenerator

Math.RandomGenerator は、Mersenne Twister 法 による乱数を発生するためのクラスです。

# Copyright notice

Mersenne Twister法の実装には
A C-program for MT19937, with initialization improved 2002/2/10. Coded by Takuji Nishimura and Makoto Matsumoto.
を改変した物を用いています。有用なプログラムソースを公開なさっている両氏に感謝します。

Copyright (C) 1997 - 2002, Makoto Matsumoto and Takuji Nishimura,
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions
are met:

1. Redistributions of source code must retain the above copyright
   notice, this list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions and the following disclaimer in the
   documentation and/or other materials provided with the distribution.
3. The names of its contributors may not be used to endorse or promote
   products derived from this software without specific prior written
   permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR
CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR
PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING
NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

# メンバ

コンストラクタ
:   [RandomGenerator](func_RandomGenerator_RandomGenerator) (環境ノイズをシードに生成 )
    [RandomGenerator](func_RandomGenerator_RandomGenerator_1) (指定シードで生成 )
    [RandomGenerator](func_RandomGenerator_RandomGenerator_2) (シリアライズコンストラクタ )

メソッド
:   [random](func_RandomGenerator_random) (0以上1.0未満の実数の乱数値を返します )
    [random32](func_RandomGenerator_random32) (0以上4,294,967,295以下 (0xffffffff 以下) の整数の乱数値を返します )
    [random63](func_RandomGenerator_random63) (0以上9,223,372,036,854,775,807以下(0x7fffffffffffffff 以下) の整数の乱数値を返します )
    [random64](func_RandomGenerator_random64) (-9,223,372,036,854,775,808以上9,223,372,036,854,775,807以下の整数の乱数値を返します )
    [randomize](func_RandomGenerator_randomize) (乱数発生器を初期化します )
    [randomize](func_RandomGenerator_randomize_1) (乱数発生器を初期化します )
    [randomize](func_RandomGenerator_randomize_2) (乱数発生器を初期化します )
    [serialize](func_RandomGenerator_serialize) (現在の状態を記録した辞書配列オブジェクトを返します )

プロパティ

イベント