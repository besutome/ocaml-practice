##自然数と再帰

前章までに扱った再帰は、リストの構造に一対一で対応した再帰だった。
次に自然数に基づいた再帰を見ていく。

##11.1　自然数の構造

無限に続く自然数。
曖昧性のない形で定義する。

*  0は自然数である
*  nが自然数ならn+1 も自然数である。

自己参照の形が現れている。再帰的なデータ型であると捉えることが出来る。

よって再帰する関数を定義できる

```ml
(*自然数は
        - 0          0あるいは
        - n +1    一つ小さい自然数nに1を加えたもの

        という形*)
```

##11.2 自然数に基づいた再帰

階乗(fact)を作ってみる。

```
n! = n * (n-1) * ... * 1
```

テスト
```
let kaizyouTest1 = fac 0 = 1
let kaizyouTest1 = fac 1 = 1
let kaizyouTest1 = fac 3 = 6
let kaizyouTest1 = fac 10 = 3628800

```
