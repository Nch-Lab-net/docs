# analogRead()

ここは`analogRead()` 関数のページです

# 説明

指定されたピンの電圧を読み取ります。Arduinoボードは複数の10bit-ADC（Analog to Digital Converter｜アナログ・デジタル変換器）を搭載しています。OVから駆動電圧（3.3Vまたは5V）の間の電圧を入力すると、それに応じた値を0から1023の整数値で返します  
Arduino UNOボードを例にすると5Vを1024分割することになるので、5/1024より訳4.9mV刻みになります  
使用可能なピン、動作電圧、分解能は下の表を参照してください

入力する電圧の範囲は[analogReference()](./../analogReference)を使用することで変更することができます
Zero、Due、MKRボードに限りますが、[analogReadResolution()](./../analogReadResolution)を使用することで分解能を変更することができます

ATMegaマイコンを搭載しているボード（UNO、Nano、mini、Mega）で`analogRead()`でアナログピンを読み取るのには100マイクロ秒ほど掛かります。そのため、1秒間で実行できる回数は最大で10,000回程度となります

| ボード |	駆動電圧 |	使用可能なピン |	最大分解能 |
|----|----|----|----|
| UNO | 5V | A0〜A5 | 10ビット |
| Mini, Nano | 5V | A0~A7 | 10ビット |
| Mega, Mega2560, MegaADK | 5V | A0~A14 | 10ビット |
| Micro | 5V | A0~A11\* | 10ビット |
| Leonardo | 5V | A0~A11\* | 10ビット |
| Zero | 3.3V | A0〜A5 | 12ビット\*\* |
| Due | 3.3V | A0~A11 | 12ビット\*\* |
| MKR Family boards | 3.3V | A0~A6 | 12ビット\*\* |

\*A0からA5は基板上の記載通りのピン、A6からA11はそれぞれ4、6、8、9、10、12番ピンで使用可能です
\*\*これらのボードのデフォルトの`analogRead()`の分解能は、互換性を確保するため10ビットとなっています。12ビットに変更するには、[analogReadResolution()](./../analogReadResolution)を使用する必要があります

# 構文

`analogRead(pin)`

# パラメータ

`pin`：電圧を読み取りたいピンの番号  
ほとんどのボードでは`A0`から`A5`、MKRボードでは`A0`から`A6`、MiniとNanoでは`A0`から`A7`、Megaでは`A0`から`A15`です

# 返り値

読み出されたアナログピンの値。A/Dコンバータの分解能によって返ってくる値の幅が異なります（10ビットなら0〜1023、12ビットなら0〜4095）  
データ型：`int`

# サンプルコード

`analogPin`の電圧を読み取り、それをシリアルモニタに表示します

```cpp
int analogPin = A3; // A3ピンに可変抵抗を接続
int val = 0;  // 読み取った値を格納する変数

void setup() {
  Serial.begin(9600);           // シリアル通信のセットアップ
}

void loop() {
  val = analogRead(analogPin);  // 入力ピンを読み取る
  Serial.println(val);          // 値をシリアルモニタに出力
}
```

# 注意点

アナログ入力ピンに何も接続されていない場合、`analogRead()`が返す値は、様々な要因（他のアナログ入力の値、ボードに手がどれだけ近いか、など）に応じて変動することになります。

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/analog-io/analogread/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
