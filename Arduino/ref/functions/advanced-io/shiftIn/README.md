# shiftIn()

ここは`shiftIn()` 関数のページです

# 説明

1バイトのデータを1ビットずつシフトさせながら受け取ります。最上位ビット（左端）または最下位ビット（右端）のどちらから読み出すかを指定できます。各ビットについて、クロックピンが`HIGH`になり、データラインから次のビットが読み出され、その後クロックピンが`LOW`になります

立ち上がりエッジでクロックを行うデバイスと接続する場合は、`shiftIn()`を最初に呼び出す前にクロックピンが`LOW`になっていることを確認する必要があります (例：`digitalWrite(clockPin, LOW)`を呼び出す)

Arduinoは、ハードウェア実装を使用するSPIライブラリも提供しており、そちらの方が高速ですが、使用できるピンは固定です

# 構文

`byte incoming = shiftIn(dataPin, clockPin, bitOrder)`

# パラメータ

`dataPin`：各ビットを入力するピンを指定します。データ型は`int`  
`clockPin`：データをシフトさせるためのクロックを送るピンを指定します  
`bitOrder`：`MSBFIRST`または`LSBFIRST`を指定し、どちらからビットを読み込むかを指定します。`MSBFIRST`は最上位ビットからの読み出し、`LSBFIRST`は最下位ビットからの読み出しを意味します  

# 返り値

読み込まれた値。型は`byte`

# 関連

[shiftOut()](./../shiftOut)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/advanced-io/shiftin/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
