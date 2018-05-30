# A-FRAME Samples

* This is a WebVR sample with A-FRAME, mainly for Oculus Go.
* これは A-Frame を利用した WebVR のサンプルで、Oculus Go を対象にしています。

## Confirmed Environment / 動作確認環境

* Chrome  66 (64-bit) for MacOS X
* Oculus Go 


## Samples / サンプル

### 360 realtime video sample / 360度リアルタイム動画

Realtime video streaming sample over WebRTC. Using following porducts, service, library.

* 360 Camera ... [RICOH THETA V](https://theta360.com/en/about/theta/v.html)
* WebRTC Platform ... [SkyWay](https://webrtc.ecl.ntt.com/en/)
* WebVR Device/Browser ... [Oculus Go](https://www.oculus.com/go/) Browser
* WebVR library ... [A-FRAME](https://aframe.io)

WebRTCを利用した360リアルタイム動画通信です。下記の製品、サービス、ライブラリを利用しています

* 360 カメラ ... [RICOH THETA V](https://theta360.com/ja/about/theta/v.html)
* WebRTC プラットフォーム ... [SkyWay](https://webrtc.ecl.ntt.com)
* WebVR デバイス/ブラウザ ... [Oculus Go](https://www.oculus.com/go/) ブラウザ
* WebVR ライブラリ ... [A-FRAME](https://aframe.io)

### How to use sample / サンプル操作手順

[GitHub pages](https://mganeko.github.io/aframe/) で試すことができます。RICOH THETA Vと Oculus Go（または他のWebVR ready のブラウザ)が必要です。

#### 配信側
* PC に RICOH THETA V をUSBで接続、Liveモードに設定
* PCのChromeブラウザで、 [https://mganeko.github.io/aframe/pc.html](https://mganeko.github.io/aframe/pc.html) を開く
  * Roomがランダムに割り振られます。変更することも可能です
* [Get Devices]ボタンをクリックすると、利用可能な Videoデバイス(カメラ)、Audioデバイス(マイク)のリストを取得します
  * カメラ、マイクへのアクセスを聞かれるので、許可してください
  * THETA V が見つかれば、自動的に選択されます
  * THETA V を接続していても検出できない場合は、Chromeを一旦終了して、再度起動して見てください
* [Start Video] ボタンをクリックしてください
  * 映像と音声が取得され、ブラウザ内に表示されます
* [Connect] ボタンをクリックしてください
  * SkyWay に接続され、指定されたRoomに参加します
  * 自分の映像の下に、Oculus Go で接続するためのURLが表示されます。
  * このURLを、Oculus Go のブラウザ（あるいは、他のWebVR 対応のブラウザ）で開くと映像を見ることができます

* 配信を停止する場合には [Disconnect] → [Stop Video] の順にボタンをクリックしてください

    
#### 視聴側 (Oculus Go)
* Oculus Go のブラウザ（あるいは、他のWebVR 対応のブラウザ）を起動してください
* 配信側で表示されたURLを、ブラウザでアクセスします
  * あらかじめ [https://mganeko.github.io/aframe/go.html?room=](https://mganeko.github.io/aframe/go.html?room=) までをブックマークに入れておき、最後にroom名だけ追加すると手間が少なくなるのでお勧めです
  * または [https://mganeko.github.io/aframe/g.html](https://mganeko.github.io/aframe/g.html) を経由してroom名を入力後、[送信]ボタンをクリックすることも可能です。
* しばらくロードの時間がかかります
  * A-FRAMEの準備ができたら 中央にメッセージが表示されます
* 画面をクリックしてください（Oculus Goのコントローラーでトリガーを引く）
  * SkyWay に接続され、指定されたRoomに参加します
  * PCに接続されている THETA V の360ど映像が表示されます
* 右下の VRモードボタンをクリックすると、360度モードになります（カーソルを合わせてOculus Goのコントローラーでトリガーを引く）
  * 自分の頭の向いている方向に応じて、映像の見える方向が変わります
* 360度モードを抜けるには コントローラの[戻る]ボタンを押します
* Skywayの接続を切る処理は未実装です。リロードするか、他のページに移動してください

### How to use sample

Please try on [GitHub pages ](https://mganeko.github.io/aframe/).
You need RICOH THETA V and Oculus Go (or other WebVR ready browser).

#### Stream 360 realtime video from PC
* Connect RICOH THETA V to your PC with USB, then start as Live mode.
* Open with desktop Chrome: [https://mganeko.github.io/aframe/pc.html](https://mganeko.github.io/aframe/pc.html)
  * Room name will be decided by random. You can modify room name if you want.
* Click [Get Devices] button, then list of video/audio devices will be made.
  * Please allow access to camera / microphone.
  * THETA V will be selected if exists.
  * If it failed to detect THETA V, pleaset quit and restart Chrome.
* Click [Start Video] button.
  * Video / Audio will be captured, and shown in the browser.
* Click [Connect] Button.
  * Connect to SkyWay, then join to the specified room.
  * URL for Oculus Go will be appear below video.
  * Open this URL with Oculus Go browser (or other WebVR ready browser), to watch 360 realtime video. (See next section)

* To stop streaming, click [Disconnect] button, then click [Stop Video] button.

#### Watch 360 realtime video with Oculus Go
* Start Oculus Go browser (or other WebVR ready browser).
* Open the URL which shown in the streaming PC.
  * It is better to bookmark [https://mganeko.github.io/aframe/go.html?room=](https://mganeko.github.io/aframe/go.html?Sroom=) in advance. Then add room name at the end of URL.
  * Or, open [https://mganeko.github.io/aframe/g.html](https://mganeko.github.io/aframe/g.html) and type room name, then submit.
* Loading will take a while.
  * When A-FRAME is ready, a message will appear in the center of browser window.
* Click the browser windows (point and trigger Oculus Go controller).
  * Connect to SkyWay, then join to the specified room.
  * 360 realtime video form the PC will be played in Oculus Go Browser.
* Click VR mode button at the right bottom corner (point and trigger Oculus Go controller), then enter 360 VR mode.
  * You can look around with Oculus Go.

* To exit 360 VR mode, push [back] button of Oculus Go controller.
* To disconnect from Skyway, please reload or move to other page.


### Source code / ソーコード

* https://github.com/mganeko/aframe
  * [pc.html](https://github.com/mganeko/aframe/blob/master/pc.html) ... Streaming 360 video, with Desktop Chrome and RICOH THETA V
  * [go.html](https://github.com/mganeko/aframe/blob/master/go.html) ... Watching 360 video, with Oculus Go or other WebVR ready Browsers


## License / ライセンス

* This sample is under the MIT license
* このサンプルはMITランセンスで提供されます



