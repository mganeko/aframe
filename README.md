# A-FRAME Samples

* This is a WebVR sample with A-FRAME, mainly for Oculus Go.
* これは A-Frame を利用した WebVR のサンプルで、Oculus Go を対象にしています。

## Confirmed Environment / 動作確認環境

* Chrome  66 (64-bit) for MacOS X
* Oculus Go 


## Samples / サンプル

### 360 realtime video sample / 360度リアルタイム動画

Realtime video streaming sample over WebRTC. Using following porducts, service, library.

* 360 Camera ... [RICHO THETA V](https://theta360.com/en/about/theta/v.html)
* WebRTC Platform ... [SkyWay](https://webrtc.ecl.ntt.com/en/)
* WebVR Device/Browser ... [Oculus Go](https://www.oculus.com/go/) Browser
* WebVR library ... [A-FRAME](https://aframe.io)

WebRTCを利用した360リアルタイム動画通信です。下記の製品、サービス、ライブラリを利用しています

* 360 カメラ ... [RICHO THETA V](https://theta360.com/ja/about/theta/v.html)
* WebRTC プラットフォーム ... [SkyWay](https://webrtc.ecl.ntt.com)
* WebVR デバイス/ブラウザ ... [Oculus Go](https://www.oculus.com/go/) ブラウザ
* WebVR ライブラリ ... [A-FRAME](https://aframe.io)

### How to use sample / サンプル操作手順

[GitHub pages](https://mganeko.github.io/aframe/) で試すことができます。RICHO THETA Vと Oculus Go（または他のWebVR ready のブラウザ)が必要です。

#### 配信側
* PC に RICHO THEATA V をUSBで接続、Liveモードに設定
* PCのChromeブラウザで、 [https://mganeko.github.io/aframe/pc.html](https://mganeko.github.io/aframe/pc.html) を開く
  * Roomがランダムに割り振られます。変更することも可能です
* [Get Devices]ボタンをクリックすると、利用可能な Videoデバイス(カメラ)、Audioデバイス(マイク)のリストを取得します
  * カメラ、マイクへのアクセスを聞かれるので、許可してください
  * THETA V が見つかれば、自動的に選択されます
* [Start Video] ボタンをクリックしてください
  * 映像と音声が取得され、ブラウザ内に表示されます
* [Connect] ボタンをクリックしてください
  * SkyWay に接続され、指定されたRoomに参加します
  * 自分の映像の下に、Oculus Go で接続するためのURLが表示されます。
  * このURLを、Oculus Go のブラウザ（あるいは、他のWebVR 対応のブラウザ）で開くと映像を見ることができます

* 配信を停止する場合には [Disconnect] → [Stop Video] の順にボタンをクリックしてください

    
#### 視聴側 (Oculus Go)
* Oculus Go のブラウザ（あるいは、他のWebVR 対応のブラウザ）を起動してください
* 配信側で表示されたURLを、ブラウザでアクセスします
  * あらかじめ [https://mganeko.github.io/aframe/go.html&room=](https://mganeko.github.io/aframe/go.html&room=) までをブックマークに入れておき、最後にroom名だけ追加すると手間が少なくなるのでお勧めです
* しばらくロードの時間がかかります
  * A-FRAMEの準備ができたら 中央にメッセージが表示されます
* 画面をクリックしてください（Oculus Goのコントローラーでトリガーを引く）
  * SkyWay に接続され、指定されたRoomに参加します
  * PCに接続されている THETA V の360ど映像が表示されます
* 右下の VRモードボタンをクリックすると、360度モードになります（カーソルを合わせてOculus Goのコントローラーでトリガーを引く）
  * 自分の頭の向いている方向に応じて、映像の見える方向が変わります
* 360度モードを抜けるには コントローラの[戻る]ボタンを押します
* Skywayの接続を切る処理は未実装です。リロードするか、他のページに移動してください


### Source code / ソーコード

* https://github.com/mganeko/aframe
  * [pc.html](https://github.com/mganeko/aframe/blob/master/pc.html) ... Streaming 360 video, with Desktop Chrome and RICHO THETA V
  * [go.html](https://github.com/mganeko/aframe/blob/master/go.html) ... Watching 360 video, with Oculus Go or other WebVR ready Browsers


## License / ライセンス

* This sample is under the MIT license
* このサンプルはMITランセンスで提供されます



