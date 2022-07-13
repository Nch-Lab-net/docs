# millis()

ここは`millis()` 関数のページです

# 説明

Arduinoボードが現在のプログラムを実行し始めてから、何ミリ秒経過したかを返します。返り値は約50日後にオーバーフローします（つまり0に戻ります）

# 構文

`time = millis()`

# パラメータ

なし

# 返り値

プログラム開始から経過した時間（ミリ秒）。型は`unsigned long`

# サンプルコード

このサンプルコードでは、Arduinoボードがコードの実行を開始してからの経過ミリ秒数をシリアルポートに表示します

```cpp
unsigned long myTime;

void setup() {
  Serial.begin(9600);
}
void loop() {
  Serial.print("Time: ");
  myTime = millis();

  Serial.println(myTime); // プログラムが始まってからの時間を表示する
  delay(1000);            // 1秒待つ
}
```

# 注意点

`millis()`の戻り値は`unsigned long`型であり、`int` 型のような小さいデータ型で演算を行おうとすると、ロジックエラーが発生する可能性があることに注意してください。また、`long`(通常の符号付き整数型)は最大値が`unsigned long`の半分であるため、`long`でもエラーが発生する可能性があります

マイクロコントローラのタイマーを再設定すると、`millis()`の読み取りが不正確になることがあります。Arduino AVRボードとArduino megaAVRボードのコアは、`millis()`の生成にTimer0を使用します。Arduino ARM (32-bits)ボードとArduino SAMD (32-bits ARM Cortex-M0+)ボードのコアはSysTickタイマーを使用します

# 関連

[micros()](./../micros)

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/time/millis/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
