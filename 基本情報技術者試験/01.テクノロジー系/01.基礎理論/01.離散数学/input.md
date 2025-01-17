# 進数の変換
## 各進数について
10進数：基数は10。桁は0～9
2進数：基数は2。桁は0と1
16進数：基数は16。桁は0～9とA～F

## コンバート方法
### 10進数から2進数へ
10進数を2で割り、その余りを求め、商が0になるまで繰り返す。余りを逆順に並べたものが2進数表現です。

### 10進数から16進数へ
10進数を16で割り、その余りを求め、商が0になるまで繰り返す。余りを逆順に並べたものが2進数表現です。

### 2進数から10進数へ
2進数の各桁に 2^3 , 2^2 , 2^1 , 2^0 を掛ける。それをSUMした値が10進数表現です。

### 2進数から16進数へ
2進数から10進数に変換して、16進数のアルファベットに対応させる。16進数が1桁の場合は左に0を加えたものが16進数表現です。

### 16進数から10進数へ
16進数の各桁に 16^1 , 16^0 を掛ける。それをSUMした値が10進数表現です。

### 16進数から2進数へ
16進数の各桁を個別に4桁の2進数に変換します。

| 16進数 | 2進数  |
|--------|--------|
| 0      | 0000   |
| 1      | 0001   |
| 2      | 0010   |
| 3      | 0011   |
| 4      | 0100   |
| 5      | 0101   |
| 6      | 0110   |
| 7      | 0111   |
| 8      | 1000   |
| 9      | 1001   |
| A (10) | 1010   |
| B (11) | 1011   |
| C (12) | 1100   |
| D (13) | 1101   |
| E (14) | 1110   |
| F (15) | 1111   |

## 練習問題
### 10進数から2進数へ

25 → 25/2=12余り1<br>
     12/2=6余り0<br>
     6/2=3余り0<br>
     3/2=1余り1<br>
     1/2=0余り1<br>

     結果.11001
---
<!-- 78 → 78/2=39余り0<br>
     39/2=19余り1<br>
     19/2=9余り1<br>
     9/2=4余り1<br>
     4/2=2余り0<br>
     2/2=0余り0<br>

     結果.001110 -->

78 → 78/2=39余り0<br>
    39/2=19余り1<br>
    19/2=9余り1<br>
    9/2=4余り1<br>
    4/2=2余り0<br>
    2/2=1余り0<br>
    1/2=0余り1<br>

    結果.1001110
---
<!-- 255 → 255/2=127余り1<br>
      127/2=63余り1<br>
      63/2=36余り1<br>
      36/2=18余り0<br>
      18/2=9余り0<br>
      9/2=4余り1<br>
      4/2=2余り0<br>
      2/2=0余り0<br>

      結果.00100111 -->

255 → 255/2=127余り1<br>
    127/2=63余り1<br>
    63/2=31余り1<br>
    31/2=15余り1<br>
    15/2=7余り1<br>
    7/2=3余り1<br>
    3/2=1余り1<br>
    1/2=0余り1<br>

    結果.11111111
---
### 10進数から16進数へ

47 → 47/16=2余り15<br>
     2/16=0余り2<br>

     結果.2F
---
123 → 123/16=7余り11<br>
      7/16=0余り7<br>

      結果.7B
---
1024 → 1024/16=64余り0<br>
       64/16=4余り0<br>
       4/16=0余り4<br>

       結果.400
---
### 2進数から10進数へ

<!-- 1011 → 1*2^3 + 0*2^2 + 1*2^1 + 1*2^0 = 8 + 0 + 2 + 0 = 10<br>

       結果.10 -->

1011 → 1*2^3 + 0*2^2 + 1*2^1 + 1*2^0 = 8 + 0 + 2 + 1 = 11<br>

       結果.11
---
11110 → 1*2^4 + 1*2^3 + 1*2^2 + 1*2^1 + 0*2^0 = 16 + 8 + 4 + 2 + 0 = 30<br>

       結果.30
---
100101 → 1*2^5 + 0*2^4 + 0*2^3 + 1*2^2 + 0*2^1 + 1*2^0 = 32 + 0 + 0 + 4 + 0 + 0 = 36<br>

       結果.36
---
### 2進数から16進数へ

1101 → 1*2^3 + 1*2^2 + 0*2^1 + 1*2^0 = 8 + 4 + 2 + 0 = 14<br>

       結果.0D
---
<!-- 111111 → 1*2^5 + 1*2^4 + 1*2^3 + 1*2^2 + 1*2^1 + 1*2^0 = 32 + 16 + 8 + 4 + 2 + 0 = 62<br>

       結果.62 -->

111111 → 1*2^5 + 1*2^4 + 1*2^3 + 1*2^2 + 1*2^1 + 1*2^0 = 32 + 16 + 8 + 4 + 2 + 1 = 63<br>
63/16=3余り15<br>
3/16=0余り3<br>

       結果.3F
---
10101010 → 1*2^7 + 0*2^6 + 1*2^5 + 0*2^4 + 1*2^3 + 0*2^2 + 1*2^1 + 0*2^0 = 128 + 0 + 32 + 0 + 8 + 0 + 2 + 0 = 170<br>
170/16=10余り10<br>
10/16=0余り10<br>

       結果.AA
---
### 16進数から10進数へ

0A → 0*16^1 + 10*16^0 = 0 + 10 =10<br>

       結果.10
---
1F → 1*16^1 + 15*16^0 = 16 + 15 = 31<br>

       結果.31
---
2A3 → 2*16^2 + 10*16^1 + 3*16^0 = 512 + 160 + 3 = 675<br>

       結果.675
---
### 16進数から2進数へ

5 → 0101<br>
1C → 0001 1100<br>
F3 → 1111 0011<br>

---
### 少数の挙動について
16進数で小数部分は、16の負のべき乗を使う<br>
小数第一位は(1/16)^1<br>
小数第二位は(1/16)^2<br>
小数第三位は(1/16)^3<br>
小数第四位は1(1/16)^4<br>

0.A → 10*1/16 = 0.625<br>
0.B → 11*1/16 = 0.6875<br>
0.C → 12*1/16 = 0.75<br>
0.D → 13*1/16 = 0.8125<br>
0.E → 14*1/16 = 0.875<br>

---
### 負数の10進数を2進数に変換する方法
10進数の-100を2進数に変換したい時には、<br>
まず100を2進数に変換してから、<br>
0,1を反転させて一回前に進める。<br>

＜例＞<br>
-100(10)を2進数に変換したい場合：<br>
100(10) = 0110 0100(2)<br>
<br>
0110 0100 → 1001 1011<br>
<br>
1001 1011 + 1 = 1001 1100<br>
<br>
結果：-100(10) = 1001 1100(2)<br>





---
# 集合論
## 集合論の記号を入力する方法について
windowsの場合は、unicodeの右側を入力してF5<br>

## 集合の種類について
### 和集合
記号：∪（２２２あ）<br>
意味：足し算<br>
式：<br>
A={1,2,3,6}, B={1,2,3,4,5}<br>
結果：<br>
1,2,3,4,5,6が返ってくる<br>

### 積積合
記号：∩（２２２９）<br>
意味：AとBに含まれる共通の値を取り出す<br>
式：<br>
A={1,2,3,4,5}, B={3}<br>
結果：<br>
3が返ってくる<br>

### 差集合
記号：\<br>
意味：Aには存在するがBには存在しない値<br>
式：<br>
A={1,2,3,4,5,6}, B={1,2,3,4,5}<br>
結果：<br>
6が返ってくる<br>

### 補集合
記号：ᶜ（１ｄ９ｃ）<br>
意味：全体集合からその値だけ取り除かれる<br>
式：<br>
Union={1,2,3,4,5}, A={1,2,3}<br>
結果：<br>
4,5,6が返ってくる<br>

### 対称差
記号：∆（２２０６）<br>
意味：どちらかには存在するが、どちらにもは存在しない値<br>
式：<br>
A={1,2,3}, B={3,4,5}<br>
結果：<br>
1,2,4,5が返ってくる<br>

### 直積
記号：×（００ｄ７）<br>
意味：マッチングアプリ<br>
式：<br>
男={1,2,3}, 女={4,5,6}<br>
結果：<br>
{(1,4),(1,5),(1,6),(2,4),(2,5),(2,6),(3,4),(3,5),(3,6)}が返ってくる<br>

### 冪（ベキ・ミャク）集合
記号：℘（２１１８）<br>
意味：フォルダ<br>
式：<br>
A={1,2}, B={3,4},C={5,6}<br>
℘(A,B,C)={1,2,3,4,5,6}<br>
結果：1,2,3,4,5,6が返ってくる<br>

### 包含関係
#### 部分集合
記号：⊆（２２８６）<br>
意味：Aに含まれる全ての値がBにも含まれている。<br>
式：<br>
A={2,3}, B={1,2,3,4,5}<br>
結果：<br>
true<br>

#### 真部分集合
記号：⊂（２２８２）≠(２２６０)<br>
意味：Aに含まれる全ての値がBにも含まれている。かつA=Bではない。<br>
式：<br>
A={2,3}, B={1,2,3,4,5}<br>
結果：<br>
A≠Bであればtrue, A=Bであればfalse<br>

#### 等集合
記号：=<br>
意味：Aの全ての値とBの全ての値が等しい場合<br>
式：<br>
A{1,2,3,4,5}, B={1,2,3,4,5}<br>
結果：<br>
true<br>

#### 不包含関係
記号：⊄（２２８４）<br>
意味：Aの中にBに含まれない値が存在している場合、AはBに包含されないと考える。<br>
式：<br>
A={1,2,3,4,5}, B={6,7,8,9,10}
結果：<br>
true<br>

#### 空集合の包含関係
記号：∅(２２０５)<br>
意味：未定義の集合。どんな集合に対しても部分集合として考える。<br>
式：<br>
A={}, B={1,2,3,4,5}<br>
結果：<br>
true<br>

## ビット演算の種類について
### AND(&)演算
説明：<br>
両方のビットが1の場合は1を返す。それ以外は0を返す。<br>
使い方：<br>
特定のビットを抽出する。マスク処理などの用途に使う。<br>
式：<br>
A=0110, B=0011<br>
結果：<br>
A&B=0010<br>

### OR(|)演算
説明：<br>
どちらか一方のビットが1なら1。<br>
使い方：<br>
ビットの結合や特定のビットをセットする。<br>
式：<br>
A=0110, B=0011<br>
結果：<br>
A|B=0111<br>

### XOR演算(^)
説明：<br>
ビットが異なるときに1。同じときは0。<br>
使い方：<br>
データの排他的な状態の確認やトグル操作。<br>
式：<br>
A=0110, B=0011<br>
結果：<br>
A^B=0101<br>

### NOT演算(~)
説明：<br>
各ビットを反転させる。0を1に、1を0に。
使い方：<br>
ビットの否定操作。<br>
式：<br>
A=0110<br>
結果：<br>
A = 1001<br>

### 左シフト演算(<<)
説明：<br>
ビット列を左に指定回数だけスライドさせる。右端の空いた桁は0で埋める。<br>
使い方：<br>
数値を2^n倍する。一回スライドで2倍、二回スライドで4倍、三回スライドで8倍になる。<br>
式：<br>
A=0110<br>
結果：<br>
A<<1=1100<br>

### 右シフト演算(>>)
説明：<br>
ビットを右に指定回数だけスライドさせる。<br>
使い方：<br>
数値を2^nで割る。<br>
式：<br>
A=0110<br>
結果：<br>
A>>1=0011<br>





# ハッシュ法
## 使い方
- データベースにパスワードを保存する
- ハッシュテーブル
- データの整合性を検証する
