# Dottie FlipFlow V1 ビルドガイド
## パーツリスト
### 共通パーツ
| Parts | Amount | Description |
| --- | --- | --- |
| PCB | 左右1枚ずつ |　キースイッチを取り付ける基板 |
| 本体ケース | 左右1つずつ | PCBを収納するケース |
| ケースヒンジ | 左右1つずつ | 左右の本体ケースをつなぐヒンジ |
| ヒンジスクリュー | 2 | ヒンジの接合部品 |
| ボトムスクリュー | 2 |　本体ケースとケースヒンジの接合部品 |
| SHケーブル | 1 | 左右PCBを接続するケーブル |
| LEDディフューザー | 1　| LEDを透過させるクリアパーツ |
| ヒンジワッシャー | 各色2 | ヒンジとヒンジスクリューに挟むワッシャー兼装飾部品 |
| ケーススペーサー | 各色2 | ケースとPCBの間に入れるスペーサー兼装飾部品 |
| マグネットDots | 各色6 | ヒンジ上部に仕込むマグネットのフタ兼装飾部品 |
| マグネットカバー | 2 | ヒンジ横に仕込むマグネットのフタ |
| サイドバー | 各色2 | ケースベゼルのスリットに差し込む装飾部品 |
|マグネット | 8 | 6 x 2 mmのマグネット |

※付属のマグネットは磁力が弱いため、100円ショップなどで購入いただくのをおすすめします。

### Standardキット(はんだ付けが必要)に含まれるパーツ
Easyキット(はんだ付け済のキット)はこれらのパーツは既にはんだ付けされているため、パーツとしては同梱されていません。
| Parts | Amount | Description |
| --- | --- | --- |
| RP2040 Zero(相当品) | 1 | マイコン |
| Kailh Choc ホットスワップソケット | 50 | キースイッチを脱着可能にするためのソケット |

### 使用者で用意するもの
| Parts | Amount | Description |
| --- | --- | --- |
| キースイッチ | 46 | Kailh Choc V1,V2, Lofree Low Profileのいずれかに対応したもの |
| キーキャップ | 1U x 44, 1.5U x 2 | Low Profileのキーキャップのみ対応 |
| ゴム足 | 8 | 装着しなくても使えますが、好みに応じてゴム足を貼り付けてください |
| USBケーブル | 1 | キーボード側はUSB Type-Cが必要 |

### 組み立てに必要な工具
| Tool | Description |
| --- | --- |
| プラスドライバー | 軸が5.5〜7mmくらいのもの |
| ニッパーもしくはカッターナイフ | PCBを切り取るために使用 |
| やすり | PCBを削るために使用 |
| ピンセット | 細かい部品をつまんだり通電確認用にあると便利 |

## 組み立てる前に
### 注意事項
- 本キーボードはヒンジ部と底面部に3Dプリント製のネジを採用していますが、強く締めるとネジ部分が固く締まったりケースが破損する可能性がありますのでご注意ください。
- 本キーボードに強い衝撃を加えると破損する恐れがあるため、特に持ち運びの際にはご注意ください。
- Standard Kitにおいても一部の部品が既にはんだ付けされていますので、はんだ付け作業の際ははんだゴテではんだ付け済みの部品に触れないように注意してください。
- 市販品のパーツ(RP2040 Zero(相当品)、ホットスワップソケット)はサービスとして添付しておりますので、万が一不良があった場合は購入者様にてご用意をお願いします。
- キーボードケースなどのSLSによる3Dプリントの部品は製造プロセス上、原料の粉末が付着している可能性があるため、その場合は布なので拭き取ってください。
- SLSによる3Dプリントの部品は形状の関係で反りなどの歪みがある場合がありますが、使用上問題ない精度であると確認したものを販売しています。気になる場合はドライヤーやヒートガンなどで温めて歪みを修正してください。

## ビルド手順
Easy Kitを購入の方ははんだ付けの手順は飛ばして本体組み立てに進んでください。

### はんだ付けの前の準備
はんだ付けの前に動作確認を行います。はんだ付けをした後に動作不良が発覚した場合、手戻りの作業に大きく時間を取られてしまうためです。  

1. RP2040 Zeroを取り出し、BOOTボタンを押下しながらPCに接続したUSBケーブル(Type-C)を接続します。
1. USBストレージとして認識されることを確認します。
1. RPI-RP2と認識されたUSBストレージにビルド済みファイルを保存します。
1. 再起動後にLEDが点灯すれば動作確認と下準備は完了です。

### はんだ付け
![はんだ付け作業で使うもの](./Images/BuildGuide01.jpg)
1. PCBの不要な部分を切り取ります。工具を使わずに切り取ることも出来ますが、ニッパーなどで切り取るときれいに仕上がります。
![切り取る前](./Images/BuildGuide02.jpg)
![切り取った後](./Images/BuildGuide03.jpg)
1. 切断面をやすりで削ります。ある程度削れていればよいです。
![削った後](./Images/BuildGuide04.jpg)
1. ホットスワップソケットのはんだ付けをします。はじめに、注意点としてソケットには向きがあります。角がある方が外側(つまりは左側)に来るようにはんだ付けします。
![エッジあるほうが左側に来るようにする](./Images/BuildGuide05.jpg)
![エッジあるほうが左側に来るようにする](./Images/BuildGuide06.jpg)

1. ホットスワップソケットをPCBに並べます。ホットスワップソケットはPCB裏面にはんだ付けします。
![](./Images/BuildGuide07.jpg)

1. ホットスワップソケットの両サイドをはんだ付けします。  
コツとしては片側だけはんだ付けした後に乗せたはんだを再加熱してホットスワップソケットを押さえるとしっかりとはんだ付けができます。  
両サイドを先にはんだ付けしてしまうと浮いていた場合に修正が難しいので片側ずつ丁寧にはんだ付けを行います。
![Right側の裏面](./Images/BuildGuide08.jpg)
![Left側の裏面](./Images/BuildGuide09.jpg)
この写真だとすべてをはんだ付けしてから浮いていないか確認していますが、これは間違いです。慣れないうちは1つ1つ確認しながらはんだ付けを行います。
![浮いてないか角度を変えてしっかり確認](./Images/BuildGuide10.jpg)

1. RP2040 Zeroをはんだ付けします。RP2040 ZeroはPCB表面にはんだ付けしてください。  
はんだ付けをする位置は意図的にずらしているので画像を参考に配置してください。
![矢印の箇所はPCBに乗せない、おしりの部分に合わせる](./Images/BuildGuide11.jpg)
1. クリアランスを確認するために1箇所だけはんだ付けし、その後ケースに入れてUSBコネクタが干渉しないか確認してください。  
干渉する場合は位置調整をしてください。
![コンパクトの代償にクリアランスが厳しくてごめんなさい](./Images/BuildGuide12.jpg)
1. 位置が確定したら残りの部分もはんだ付けします。
![使用するIOが少ないので画像では全部ははんだ付けしてません](./Images/BuildGuide13.jpg)

はんだ付けの作業はここで終了です。続きまして本体の組み立てです。

### 本体組み立て

![本体の組み立て作業で使うもの](./Images/BuildGuide14.jpg)
1. ケースヒンジ(左側)を裏返し、LEDディフューザーを差し込みます。抜けないようクリアランスがシビアになっているため破損させないようゆっくりと押し込んでください。
![固いのでグッと押し込みます](./Images/BuildGuide15.jpg)

1. ヒンジスクリューにヒンジワッシャーを差し込みます。  
ヒンジワッシャーは色違いを用意していますのでお好きなカラーをお選びください。
![グッと押し込みます](./Images/BuildGuide16.jpg)

1. 左右のケースヒンジを組み合わせ、ヒンジスクリューで止めます。  
このとき、強く締めないでください！ヒンジ部はネジの圧力によって破損する恐れがあるので、ヒンジを開閉させながら締め具合を微調整してください。

![ヒンジスクリューを優しく締めます](./Images/BuildGuide17.jpg)
![フェザータッチで締めてください](./Images/BuildGuide18.jpg)

1. マグネットDotsを取り付けます。このとき、マグネットがある場合は先に赤丸の箇所にマグネットを入れてからマグネットDotsを取り付けてください。  
マグネットを利用する場合は磁力でくっつくよう方向を確認しながら入れてください。
![赤丸はマグネットを入れる箇所](./Images/BuildGuide19.jpg)
![お好きなカラーのマグネットDotsをお選びください](./Images/BuildGuide20.jpg)
![表面からみるとこんな感じ](./Images/BuildGuide21.jpg)

1. ケースヒンジの横部にマグネットカバーを取り付けます。このとき、マグネットがある場合は先に赤丸の箇所にマグネットを入れてからマグネットカバーを取り付けてください。  
マグネットを利用する場合は磁力でくっつくよう方向を確認しながら入れてください。
![赤丸はマグネットを入れる箇所](./Images/BuildGuide22.jpg)
![マグネットカバーを装着するとこんな感じ](./Images/BuildGuide23.jpg)

1. サイドバーを装着します。ケースサイドのスリットはサイドバーを装着しなくても見栄えがいいのでこちらについてはお好みで装着してください。  
装着する場合はサイドバーをスリットの形状に合わせて押し込みます。

![軽く差し込んでから](./Images/BuildGuide24.jpg)
![グッと押し込む](./Images/BuildGuide25.jpg)

1. SHケーブルをPCBに差し込みます。その前に、差し込むコネクタの向きを確認します。  
SHケーブルのコネクタは金具が見えている面とプラスチック面がありますが、写真にある通りプラスチック面がみえるように差し込みます。
![差し込む向きを間違えると故障の恐れがあるため注意が必要です](./Images/BuildGuide26.jpg)
![向きがあってるとしっかりと刺さります](./Images/BuildGuide27.jpg)
PCBの左側にSHケーブルを差し込んでからケーススペーサーを乗せます。ケーブルを差し込みましたら四角のホールにケーブルを通しておきます。
![お好きなカラーのケーススペーサーをお選びください](./Images/BuildGuide28.jpg)

1. PCBを置いたまま本体ケース(左側)をPCBに差し込みます。一気に差し込むのではなく2/3くらいまで差し込んでください。  
このとき、本体ケースにPCBが入りづらい場合は何度か抜き差しをして馴染ませてください。もしくはPCBの切り取り箇所が引っかかっていないかも合わせて確認してください。
![](./Images/BuildGuide29.jpg)

1. PCBを本体ケース奥まで差し込みます。ケーススペーサーがズレていないことも確認してください。
![奥まで差し込むとケーススペーサーと本体ケースの穴の位置が合います](./Images/BuildGuide30.jpg)
![ケーブルを挟み込んでいないか表面からも確認する](./Images/BuildGuide31.jpg)

1. SHケーブルをケースヒンジ内に通します。赤囲み箇所の切り欠きにケーブルを挿入します。
![ほんとにケーブル通るの？となりそうですが、とりあえず突っ込んでみる](./Images/BuildGuide32.jpg)
ケーブルが反対側から出ていることを確認します。うまく出てこない場合はピンセットなどでやさしく引き上げてください。  
強くひっぱるとコネクタ部分が破損するので注意してください。
![意外とコネクタがスッと出てくる](./Images/BuildGuide33.jpg)

1. SHケーブルが反対側に通ったら本体ケースとケースヒンジに差し込みます。このとき、ケーブルが抜けないよう注意しながら本体ケースを差し込んでください。
![合体っっ！！！](./Images/BuildGuide34.jpg)

1. 本体ケースにボトムスクリューで止めます。ヒンジスクリューと同様、締めすぎに注意してください。
![](./Images/BuildGuide35.jpg)

1. PCB(右側)にSHケーブルを差し込みます。左側と同様、プラスチック面がみえるようにして差し込んでください。ケーブルを差し込んだらケーススペーサーを置きます。
![](./Images/BuildGuide36.jpg)

1. PCB(右側)に本体ケースを差し込みます。手順は左側と同様です。差し込んだら同様にボトムスクリューで止めてください。
![](./Images/BuildGuide37.jpg)
![](./Images/BuildGuide38.jpg)

1. これで完成です！
お好きなキースイッチとキーキャップを装着してください！！ 
![](./Images/BuildGuide39.jpg)