# map()

ここは`map()` 関数のページです

# 説明

ある範囲から別の範囲に数値をマッピングします。つまり、`fromLow`の値は`toLow`に、`fromHigh`の値は`toHigh`に、`fromLow`と`fromHigh`の中間の値は`toLow`と`toHigh`の中間の値に変換されます  
引数で指定された値が`fromLow`と`fromHigh`の範囲外だった場合は`toLow`と`toHigh`の範囲外の値に変換されます。つまり、[constrain()](./../constrain)のように値を特定の範囲外に制限するようなことはしません  
範囲に制限を設けたい場合は前後で`constrain()`を使用することで実現できます

尚、各引数の下限値、上限値の関係は必ずしも`下限値 ＜ 上限値`である必要はないため、以下のようにして`map()`を用いて数値の範囲を反転させることもできます

```cpp
y = map(x, 1, 50, 50, 1);
```

この関数は負の数も扱うことができるように作られています。そのため以下のようなコードも正常に動作します

```cpp
y = map(x, 1, 50, 50, -100);
```

`map()`は整数で演算を行うため、数学的には分数となる場合でも整数が返されます。小数点以下の端数が発生する場合はすべて切り捨てられます

# 構文

`map(value, fromLow, fromHigh, toLow, toHigh)`

# パラメータ

`value`：マッピングさせたい値
`fromLow`：マッピングする前の値の範囲の下限
`fromHigh`：マッピングする前の値の範囲の上限
`toLow`：マッピングした後の値の範囲の下限
`toHigh`：マッピングした後の値の範囲の上限


# 返り値

マッピングされた値

# サンプルコード

このコードでは10bitのアナログ入力の値を8bitの範囲に変換しています

```cpp
void setup() {}

void loop() {
  int val = analogRead(0);
  val = map(val, 0, 1023, 0, 255);
  analogWrite(9, val);
}
```

# 補足

数学が好きな方のために、関数の構造を以下に示します

```cpp
long map(long x, long in_min, long in_max, long out_min, long out_max) {
  return (x - in_min) * (out_max - out_min) / (in_max - in_min) + out_min;
}
```

# 注意点

前述の通り、この関数は整数で演算を行います。そのため、分数が頻繁に発生する場合は思ったとおりに動かないことがあります  
例えば、3/2, 4/3, 5/4 のような分数は、実際の値が異なるにもかかわらず、`map()`関数からすべて 1 として返されます  
そのため、正確な計算結果を必要とする場合（例：小数点以下3桁までの正確な電圧）は`map()`の使用を避け、手動で実装することを検討してください

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/math/map/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
