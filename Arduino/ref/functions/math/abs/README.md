# abs()

ここは`abs()` 関数のページです

# 説明

数値の絶対値を計算します

# 構文

`abs(x)`

# パラメータ

`x`：絶対値を求めたい数字

# 返り値

`x`の絶対値  
`x ≧ 0`ならば`x`、`x ＜ 0`ならば`-x`を返します

# サンプルコード

変数`x`の絶対値をシリアルモニタに表示します

```cpp
void setup() {
  Serial.begin(9600);
  while (!Serial) {
    ;  // シリアルポートに接続されるのを待ちます
  }
  int x = 42;
  Serial.print("The absolute value of ");
  Serial.print(x);
  Serial.print(" is ");
  Serial.println(abs(x));
  x = -42;
  Serial.print("The absolute value of ");
  Serial.print(x);
  Serial.print(" is ");
  Serial.println(abs(x));
}

void loop() {
}
```

# 注意点

`abs()`の実装の都合上、括弧内で他の関数を使用するのは避けてください。誤った結果を返す可能性があります

```cpp
abs(a++); // これは避けてください

// その代わり以下の方法を使用してください
abs(a);
a++;  // 計算をabs関数の外に置く
```

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/math/abs/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
