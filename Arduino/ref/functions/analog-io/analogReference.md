# analogReference()

ここは`analogReference()` 関数のページです

# 説明

アナログ入力に使用される基準電圧（入力範囲の上限として使用される値）を設定します。オプションは以下の通りです

Arduino AVR Boards (Uno, Mega, Leonardo など)

- `DEFAULT`: 5V(5V Arduinoボード上)または3.3V(3.3V Arduinoボード上)の規定の基準電圧を指定します
- `INTERNAL`: 内蔵の基準電圧を指定します。ATmega168とATmega328Pで1.1V、ATmega32U4とATmega8で2.56Vになります (Arduino Megaでは利用できません)
- `INTERNAL1V1`: 内蔵の1.1Vの基準電圧を指定します(Arduino Megaのみ)
- `INTERNAL2V56`: 内蔵の2.56Vの基準電圧を指定します(Arduino Megaのみ)
- `EXTERNAL`: `AREFピン`に印加される電圧(0V～5V)を基準電圧として指定します

Arduino SAMD Boards (Zero など)

- `AR_DEFAULT`：デフォルトのアナログ基準電圧3.3V
- `AR_INTERNAL`：2.23Vの内蔵リファレンス
- `AR_INTERNAL1V0`: 1.0Vの内蔵リファレンス
- `AR_INTERNAL1V65`：1.65Vの内蔵リファレンス
- `AR_INTERNAL2V23`：2.23Vの内蔵リファレンス
- `AR_EXTERNAL`：AREF端子に印加される電圧

Arduino megaAVR Boards (Uno WiFi Rev2)

- `DEFAULT`：0.55Vの内蔵リファレンス
- `INTERNAL`：0.55Vの内蔵リファレンス

VDD: ATmega4809のVdd。Uno WiFi Rev2では5V。

- `INTERNAL0V55`：0.55Vの内蔵リファレンス
- `INTERNAL1V1`：1.1Vの内蔵リファレンス
- `INTERNAL1V5`：1.5Vの内蔵リファレンス
- `INTERNAL2V5`：2.5Vの内蔵リファレンス
- `INTERNAL4V3`：4.3Vの内蔵リファレンス
- `EXTERNAL`：AREF端子に印加される電圧（0V〜5V）

Arduino SAM Boards (Due)

- `AR_DEFAULT`：3.3V のデフォルトのアナログ基準。これはDueで唯一サポートされているオプションです

Arduino Mbed OS Nanoボード（Nano 33 BLE）、Arduino Mbed OS Edgeボード（Edge Control）

- `AR_VDD`: デフォルトの3.3Vリファレンス
- `AR_INTERNAL`: 0.6Vの内蔵リファレンス
- `AR_INTERNAL1V2`: 1.2Vリファレンス (内蔵の0.6Vのリファレンス電圧を2倍に増幅したもの)
- `AR_INTERNAL2V4`: 2.4Vリファレンス (内蔵の0.6Vのリファレンス電圧を4倍に増幅したもの)

# 構文

`analogReference(type)`

# パラメータ

`type`：使用するタイプのリファレンス（[説明](#説明)を参照してください）

# 返り値

なし

# 注意点

アナログリファレンスを変更した後、`analogRead()`からの最初の数回の読み取りが正確でない場合があります

**AREFピンの外部基準電圧に0V未満または5V以上のものを決して使用しないでくださいAREFピンで外部リファレンスを使用する場合は、`analogRead()`を呼び出す前に`analogReference()`を`EXTERNAL`に設定する必要があります**
そうしないと、アクティブリファレンス電圧（内部生成）とAREF端子がショートしてしまい、Arduinoボード上のマイコンにダメージを与える可能性があります

また、外部基準電圧を5kΩの抵抗を介して`AREFピン`に接続することで、外部基準電圧と内部基準電圧を切り替えて使用することもできます。`AREFピン`には32Kの内部抵抗があるため、抵抗によってリファレンスとして使用される電圧が変化することに注意してください。この2つは分圧器として機能するため、例えば、抵抗を通して2.5Vを印加すると、AREFピンには`2.5 * 32 / (32 + 5) = 約2.2V`が印加されます

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/analog-io/analogreference/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://pages.nchlab.net/Arduino/ref/)  
[トップページに戻る](https://pages.nchlab.net/)
