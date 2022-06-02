# Arduino Reference

Arduinoの各種関数の日本語リファレンス

# Arduino標準関数

[Arduino公式ページ](https://www.arduino.cc/reference/en/)に記載があるものを標準関数としています

## **デジタル入出力**

[pinMode()](./functions/digital-io/pinMode)  
[digitalRead()](./functions/digital-io/digitalRead)  
[digitalWrite()](./functions/digital-io/digitalWrite)  
[デジタルピンの説明](./functions/digital-io/digital-pins)  

## **アナログ入出力**

[analogReference()](./functions/analog-io/analogReference)  
[analogRead()](./functions/analog-io/analogRead)  
[analogReadResolution()](./functions/analog-io/analogReadResolution)  
[analogWrite()](./functions/analog-io/analogWrite)  
[analogWriteResolution()](./functions/analog-io/analogWriteResolution)  

## **高度な入出力**

[tone()](./functions/advanced-io/tone)  
[noTone()](./functions/advanced-io/noTone)  
[pulseIn()](./functions/advanced-io/pulseIn)  
[pulseInLong()](./functions/advanced-io/pulseInLong)  
[shiftIn()](./functions/advanced-io/shiftIn)  
[shiftOut()](./functions/advanced-io/shiftOut)  

## **時間**

[delay()](./functions/time/delay)  
[delayMicroseconds()](./functions/time/delayMicroseconds)  
[micros()](./functions/time/micros)  
[millis()](./functions/time/millis)  

## **計算**

[abs()]()  
[constrain()]()  
[map()]()  
[max()]()  
[min()]()  
[pow()]()  
[sq()]()  
[sqrt()]()  

## **三角関数**

[sin()]()  
[cos()]()  
[tan()]()  

## **文字**

[isAlpha()]()  
[isAlphaNumeric()]()  
[isAscii()]()  
[isControl()]()  
[isDigit()]()  
[isGraph()]()  
[isHexademicalDigit()]()  
[isLowerCase()]()  
[isPrintable()]()  
[isPunct()]()  
[isSpace()]()  
[isUpperCase()]()  
[isWhitespace()]()  

## **乱数**

[random()]()  
[randomSeed()]()  

## **ビット・バイト**

[bit()]()  
[bitClear()]()  
[bitRead()]()  
[bitSet()]()  
[bitWrite()]()  
[highByte()]()  
[lowByte()]()  

## **外部割り込み**

[attachInterrupt()]()  
[detachInterrupt()]()  

## **割り込み**

[interrupts()]()  
[noInterrupts()]()  

## **通信**

[Serial()]()  
[SPI()]()  
[Stream()]()  
[Wire()]()  

## **USB**

[Keyboard()]()  
[Mouse()]()  

# Arduinoで使える変数

## **定数**

[HIGH]()｜[LOW]()  
[INPUT]()｜[OUTPUT]()｜[INPUT_PULLUP]()  
[LED_BUILTIN]()  
[true]()｜[false]()  
[浮動小数点型]()  
[整数型]()  

## **型変換**

[(unsigned int)]()  
[(unsigned long)]()  
[byte()]()  
[char()]()  
[float()]()  
[int()]()  
[long()]()  
[word()]()  

## **データ型**

[配列]()  
[bool]()  
[boolean]()  
[byte]()  
[char]()  
[double]()  
[float]()  
[int]()  
[long]()  
[short]()  
[size_t]()  
[string]()  
[String()]()  
[unsigned char]()  
[unsigned int]()  
[unsigned long]()  
[vold]()  
[word]()  

## **変数のスコープと修飾子**

[const]()  
[scope]()  
[static]()  
[volatile]()  

## **ユーティリティ**

[PROGMEM]()  
[sizeof()]()  

# Arduinoの構造

## **スケッチ**

[loop()]()  
[setup()]()  

## **制御構造**

[break]()  
[continue]()  
[do...while]()  
[else]()  
[for]()  
[goto]()  
[if]()  
[return]()  
[switch...case]()  
[while]()  

## **その他の構文**

[#define]()  
[#include]()  
[/\* \*/]()  
[//]()  
[;]()  
[{}]()  

## **算術演算子**

[%]()  
[\*]()  
[+]()  
[-]()  
[/]()  
[=]()  

## **比較演算子**

[!=]()  
[<]()  
[<=]()  
[==]()  
[>]()  
[>=]()  

## **論理演算子**

[!]()  
[&&]()  
[||]()  

## **ポインタ・アクセス演算子**

[&]()  
[*]()  

## **ビット演算子**

[&]()  
[<<]()  
[>>]()  
[^]()  
[|]()  
[~]()  

## **複合演算子**

[%=]()  
[&=]()  
[\*=]()  
[++]()  
[+=]()  
[--]()  
[-=]()  
[/=]()  
[^=]()  
[|=]()  

# 出典

このページは[Arduino公式のページ](https://arduino.cc/reference/en/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)
