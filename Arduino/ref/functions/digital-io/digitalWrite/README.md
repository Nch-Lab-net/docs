# digitalWrite()

ここは`digitalWrite()` 関数のページです

# 説明

`HIGH`または`LOW`をデジタルピンから出力します  
指定したピンが[pinMode()](./../pinMode)によって出力に設定されている場合、そのピンの出力は指定された値に対応する電圧となります  
`HIGH`：電源電圧（5Vボードの場合は5V、3.3Vボードの場合は3.3V）  
`LOW`：0V（GND電位に等しい）  

ピンが入力に設定されている状態で`digitalWrite()`を実行すると、そのピンの内蔵プルアップ抵抗を操作することになります。`HIGH`は有効、`LOW`は無効にそれぞれ対応しています  
ただし、内部プルアップ抵抗を有効にしたい場合`pinMode()`で`INPUT_PULLUP`を指定することをオススメします。詳細は[デジタルピン](./../digital-pins)を参照してください  

`pinMode()`を`OUTPUT`にしていない状態でLEDに接続されたピンに対し`digitalWrite(pin, HIGH)`を実行するとLEDが薄暗く点灯することがあります。これは内部プルアップ抵抗が大きな値をもつ電流制限抵抗のように動作するからです  
これを避けるため、`pinMode()`で明示的に`OUTPUT`に設定する必要があります  

# 構文

`digitalWrite(pin, value)`

# パラメータ

`pin`：Arduinoのデジタルピンの番号  
`vaiue`：`HIGH`または`LOW`  

# 返り値

なし

# サンプルコード

このコードでは13番ピンを`OUTPUT`として使用し、`HIGH`と`LOW`を1秒ごとに切り替えます

```cpp
void setup() {
  pinMode(13, OUTPUT);     //  13番ピンをOUTPUTに設定
}

void loop() {
  digitaiWrite(13, HIGH);  //  13番ピンをHIGHに設定
  delay(1000);             //  1000ミリ秒待つ
  digitaiWrite(13,  LOW);  //  13番ピンを LOWに設定
  delay(1000);             //  1000ミリ秒待つ
}
```

# 注意点

アナログ入力ピンは、`A0` `A1`のように指定することでデジタルピンとして使用できます。だたし、アナログ入力としてのみ使用できるArduino Nano、Pro Mini、およびMiniの`A6`および`A7`ピンを除きます

# 関連

[デジタルピンの説明](./../digital-pins)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/digital-io/digitalwrite/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
