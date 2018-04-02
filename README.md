# ESP32_bt_speaker
bluetooth speaker using I2S + built in DAC

* esp-idfのexamples/bluetooth/a2dp_sinkを元に、ESP32内蔵DACから音声を出力します。
* esp-idf環境用です。

2018年2月20日(火)追記

* esp-idfが、かなり変更されたので更新しました。
* esp-idfのexamples/bluetooth/a2dp_sinkがDAC/I2S DA
　出力をサポートしたけど、まだ動かないので、
　これを動くように修正したものに置き換えました。
* 以下の問題が残っています。解決策をご存じの方は、教えていだけますとありがたいです。
  * 音量を上げると音が割れる問題
  * 音の出力先を変えるなどして 通信がsuspendすると変な音が出続ける問題 (DMAバッファに音データが残る？)

2018年4月2日(月)追記

 * main/Kconfig.projbuild の追加忘れで、うまくコンパイル出来ない問題を修正しました。
 * 初回make時、或いはmake menuconfigの設定画面で
  * A2DP Example Configuration --> を選択
  * A2DP Sink  Output (Internal DAC) ---> を選択
  * Internal DAC を選択してください。
  * Serial Flasher configでシリアルポートの設定も行ってください。

<img src="https://github.com/h-nari/ESP32_bt_speaker/blob/master/img/sc180402a1.PNG?raw=true"/>

<img src="https://github.com/h-nari/ESP32_bt_speaker/blob/master/img/sc180402a2.PNG?raw=true" />

<img src="https://github.com/h-nari/ESP32_bt_speaker/blob/master/img/sc180402a3.PNG?raw=true" />


## 接続

<img src="https://github.com/h-nari/ESP32_bt_speaker/blob/master/img/sc170503a1.png?raw=true" width="400"/>

* 半固定抵抗ではなく、100Ωと1KΩで1/10程度に固定比で分圧しても問題ないと思います。
* コンデンサの容量は 10uF程度にした方が音質がよくなるかもしれません。

## デモ動画

* <a href="https://youtu.be/7-ZSAkkyPiY">ESP32内蔵DA出力Bluetooth speaker</a>
