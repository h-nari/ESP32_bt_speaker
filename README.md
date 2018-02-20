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

## 接続

<img src="https://github.com/h-nari/ESP32_bt_speaker/blob/master/img/sc170503a1.png?raw=true" width="400"/>

* 半固定抵抗ではなく、100Ωと1KΩで1/10程度に固定比で分圧しても問題ないと思います。

## デモ動画

* <a href="https://youtu.be/7-ZSAkkyPiY">ESP32内蔵DA出力Bluetooth speaker</a>
