# analogWrite()

ここは`analogWrite()` 関数のページです

# 説明

PWM（Pulse Width Modulation｜パルス幅変調）でアナログ電圧を出力します。LEDを光らせる明るさを変えたり、モータを回転させる速さを変えたりするのに使用することができます  
ピンに対し`analogWrite()`を実行した後、同じピンに再度`analogWrite()`を実行する、または`digitalRead()`や`digitalWrite()`を実行するまでは指定したduty比の矩形波を出力し続けます

以下に各ボードでPWM出力ができるピンと出力される矩形波の周波数を示します

| ボード |  PWM ピン | PWM 周波数 |
|----|----|----|
| Uno, Nano, Mini | 3, 5, 6, 9, 10, 11 | 490Hz (5, 6番ピン: 980Hz) |
| Mega | 2〜13, 44〜46 | 490Hz (4, 13番ピン: 980Hz) |
| Leonardo, Micro, Yún | 3, 5, 6, 9, 10, 11, 13 | 490 Hz (3, 11番ピン: 980Hz) |
| Uno WiFi Rev2, Nano Every | 3, 5, 6, 9, 10 | 976Hz |
| MKR boards \* | 0〜8, 10, A3, A4 | 732Hz |
| MKR1000 WiFi \* | 0〜8, 10, 11, A3, A4 | 732Hz |
| Zero \* | 3〜13, A0, A1 | 732Hz |
| Nano 33 IoT \* | 2, 3, 5, 6, 9〜12, A2, A3, A5 | 732Hz |
| Nano 33 BLE/BLE Sense | 1〜13, A0〜A7 | 500Hz |
| Due \*\* | 2〜13 | 1000Hz |
| 101 | 3, 5, 6, 9 | 3, 9番ピン: 490 Hz、5, 6番ピン: 980Hz |

\* MKR、Nano 33 IoT、Zeroの各ボードでは、上記のピンのPWM機能に加えて、DAC0（A0）ピンで`analogWrite()`を実行すると、真のアナログ出力ができます
\*\* Dueの場合、上記のピンのPWM機能に加えて、DAC0とDAC1ピンで`analogWrite()`を実行すると、真のアナログ出力ができます

`analogWrite()`を呼ぶ前に、`pinMode()`を呼んでピンを出力に設定する必要はありません。
`analogWrite()`関数は、アナログピンや `analogRead()`関数とは何の関係もありません。

# 構文

`analogWrite(pin, value)`

# パラメータ

`pin`：PWM出力をさせたいピン。データ型は`int`  
`value`：出力する値。0（常にオフ）〜255（常にオン）。データ型は`int`

# 返り値

なし

# サンプルコード

可変抵抗から読み取った値に比例してLEDを調光させます

```cpp
int ledPin = 9;      // 9番ピンにLEDを接続
int analogPin = 3;   // 3番ピンに可変抵抗を接続
int val = 0;         // 読み取った値を格納する変数

void setup() {
  pinMode(ledPin, OUTPUT);  // ピンを出力に設定
}

void loop() {
  val = analogRead(analogPin);  // 入力ピンを読み取る
  analogWrite(ledPin, val / 4); // analogReadの値は0〜1023、analogWriteの値は0〜255
}
```

# 注意点

5, 6番ピンで生成されるPWM出力の周波数が他のピンより高くなっています。これは、これらのPWM出力を生成するために使用されるのと同じ内部タイマーを共有する`millis()`関数と`delay()`関数との相互作用によるものです。これは、低duty比の状況（例：0～10）で顕著に現れ、5, 6番ピンから0を出力したとき出力が完全にオフにならない可能性があります

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/analog-io/analogwrite/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://pages.nchlab.net/Arduino/ref/)  
[トップページに戻る](https://pages.nchlab.net/)
