# delayMicroseconds()

ここは`delayMicroseconds()` 関数のページです

# 説明

引数で指定された時間（マイクロ秒）だけ、プログラムを一時停止します
1ミリ秒は1,000マイクロ秒、1秒は1,000,000(100万)マイクロ秒です

現在、正確に動作する最大の値は`16383`です。これより大きな値を設定すると、極端に短い遅延になることがあります。そのため、数千マイクロ秒以上を指定したい場合は`delayMicroseconds()`の代わりに`delay()`を使用する必要があります

# 構文

`delayMicroseconds(us)`

# パラメータ

`us`：停止させたい時間（マイクロ秒）。型は`unsigned int`  

# 返り値

なし

# サンプルコード

このコードでは、ピン番号8が出力ピンとして動作するように設定し、約100マイクロ秒周期のパルス列を送信します

```cpp
int outPin = 8;               // 8番ピンを使用

void setup() {
  pinMode(outPin, OUTPUT);    // デジタルピンを出力2設定
}

void loop() {
  digitalWrite(outPin, HIGH); // デジタルピンをオンに
  delayMicroseconds(50);      // 50マイクロ秒待つ
  digitalWrite(outPin, LOW);  // デジタルピンをオフに
  delayMicroseconds(50);      // 50マイクロ秒待つ
}
```

# 注意点

この関数は、3から16383までの範囲で非常に正確に動作します。これより小さい遅延時間では、`delayMicroseconds()`が正確に動作することを保証することはできません。より大きな遅延時間では、実際には極めて短い時間しか遅延しない可能性があります

Arduino 0018で、`delayMicroseconds()`が割り込み禁止にならなくなりました

今後のArduinoのリリースで仕様が変更される可能性があります

# 関連

[delay()](./../delay)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/time/delaymicroseconds/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
