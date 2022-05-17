# Spreadwriter

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/02.jpg?raw=true" width="600px"/>

"Spreadwriter" は[GL516ケース](https://shop.yushakobo.jp/products/3814)に対応した50%キーボードです。  
放射状のキーレイアウトは、手を自然な形で置くことができ、楽な姿勢での打鍵を可能にしています。  
LEDを用いたキーの照明や、ロータリーエンコーダの搭載も可能です。

"Spreadwriter" is a 50% keyboard for the [GL516 case](https://shop.yushakobo.jp/products/3814).  
The radial key layout allows for a natural hand placement and comfortable typing posture.  
LED-based key illumination and a rotary encoder are also available.  

GL516ケースについての説明は[こちら](https://salicylic-acid3.hatenablog.com/entry/gl516-introduction)をご覧ください・

## 必要な部品

### キットに同梱されているもの
|部品|個数|備考|
|:--|:--|:--|
|PCB|1|リードタイプと表面実装のダイオードに対応。|
|キースイッチプレート|1||
|デコレーションプレート|1||

### ご自身で用意が必要なもの
|部品|個数|備考|
|:--|:--|:--|
|[GL516ケース](https://shop.yushakobo.jp/products/3814)|1|付属している各種プレートやネジなども組み立てに使用します。|
|ダイオード|54|[リードタイプ](https://shop.yushakobo.jp/products/a0800di-01-100)と[SMDタイプ](https://shop.yushakobo.jp/products/a0800di-02-100)に対応しております。|
|[タクタイルスイッチ](https://shop.yushakobo.jp/products/a0800ts-01-1)|1|リセットスイッチとして利用します。|
|キーキャップ 1u|49|Cherry MX軸に対応したもの。|
|キーキャップ 1.25u|2|Cherry MX軸に対応したもの。|
|キーキャップ 1.5u|2|Cherry MX軸に対応したもの。|
|キースイッチ|53|Cherry MX互換のもの。|
|ロータリーエンコーダ|1|ノブは直径16.5mm以下に対応しております。|
|[スイッチ用 ソケット(MX)](https://shop.yushakobo.jp/products/a01ps)|53||
|[Pro Micro](https://shop.yushakobo.jp/search?q=Pro+Micro)|1||
|USBケーブル|1|Pro MicroとPCを接続します。|

### オプション
|部品|個数|備考|
|:--|:--|:--|
|[BLE Micro Pro](https://shop.yushakobo.jp/products/ble-micro-pro)|1|[GL516の無線用電池部品セットと無線用単4電池ケース](https://booth.pm/ja/items/3675855)に対応しております。|
|コンスルー|2||
|[SK6812MINI-E](https://shop.yushakobo.jp/products/sk6812mini-e-10)|53|キーキャップを底面から照らすバックライト。|

## 組み立て方

- 基本的な組立方法は[自作キーボードキット『A52GL』『J73GL』ビルドガイド](https://salicylic-acid3.hatenablog.com/entry/a52gl-j73gl-build-guide)と同様です。
- BLE Micro Proを用いて無線化する際は[GL516 カスタマイズガイド](https://zenn.dev/salicylic_acid3/books/gl516_customize_guide)をご覧ください。

### 1. PCBの裏面にダイオードをはんだ付けする

#### a. リードタイプのダイオードをハンダ付けする場合

<!--
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0581.jpg?raw=true" width="600px"/>
-->

ダイオードをPCBのハンダづけ用の穴に挿し込めるように曲げます。  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0583.jpg?raw=true" width="600px"/>

ダイオードをPCBに挿し込みます。  
ダイオードの黒線がPCBの　`▷|` の向き先と合うように配置します。  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0585.jpg?raw=true" width="600px"/>

PCBの表面からダイオードの足が出ていることを確認します。  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0586.jpg?raw=true" width="600px"/>

ダイオードの足をPCBにハンダ付けし、ニッパーで足を切ります。  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0587.jpg?raw=true" width="600px"/>

全部で54箇所をハンダ付けします。

#### b. SMDタイプのダイオードをハンダ付けする場合

ダイオードの線とPCBの　`▷|` の向き先と合うように配置します。  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0588.jpg?raw=true" width="600px"/>

下記の動画のように、予備ハンダ(事前にハンダをハンダ箇所に乗せておき、溶かしながらハンダ付けを行う)を行いながらピンセットを使いながらハンダ付けを行うとスムーズに作業が進められます。  
https://user-images.githubusercontent.com/4215759/126895350-43ae4cd4-408b-4ff4-ab5c-2903e0420978.mov

<!--
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0590.jpg?raw=true" width="600px"/>
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0591.jpg?raw=true" width="600px"/>
-->

このようにSMDダイオードの両端をPCBにハンダ付けできれば完了です。  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0592.jpg?raw=true" width="600px"/>

全部で54箇所をハンダ付けします。

### リセットスイッチの取り付け

リセットスイッチの取付箇所は、PCB裏面の中央部奥側です。  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0595.jpg?raw=true" width="600px"/>

リセットスイッチのボタンの天面がPCB裏面方向になるように挿し込みます。  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0596.jpg?raw=true" width="600px"/>

PCBの表面は下図のようになります。  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0597.jpg?raw=true" width="600px"/>

足が出ていることを確認したら、ハンダ付けを行います。  
マスキングテープなどでリセットスイッチを固定すると、作業がスムーズに進められます。  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0598.jpg?raw=true" width="600px"/>


### Pro Microの取り付け

Pro MicroはPCB裏面に取り付けます。
Pro Microの各ピンの番号とPCB穴の印字が合うように挿し込んでください。  
(Pro Microの機種にもよりますが、大抵のものはチップが配置されている側がPCB裏面と同じ向きになるように挿し込みます。)  
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0603.jpg?raw=true" width="600px"/>

### ファームウェアの書き込み

### LEDの取り付け (上級者向け)

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0579_b.jpg?raw=true" width="600px"/>

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0607.jpg?raw=true" width="600px"/>

### スイッチソケットの取り付け

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0599.jpg?raw=true" width="600px"/>

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0600.jpg?raw=true" width="600px"/>

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0601.jpg?raw=true" width="600px"/>

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0602.jpg?raw=true" width="600px"/>

### ロータリーエンコーダの取り付け


<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0619.jpg?raw=true" width="600px"/>
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0618.jpg?raw=true" width="600px"/>

### キースイッチプレートの取り付け

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0611.jpg?raw=true" width="600px"/>

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0613.jpg?raw=true" width="600px"/>

### GL516ケースへの取り付け

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0614.jpg?raw=true" width="600px"/>

<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_0622.jpg?raw=true" width="600px"/>



<!--
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_.jpg?raw=true" width="600px"/>
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_.jpg?raw=true" width="600px"/>
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_.jpg?raw=true" width="600px"/>
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_.jpg?raw=true" width="600px"/>
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_.jpg?raw=true" width="600px"/>
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_.jpg?raw=true" width="600px"/>
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_.jpg?raw=true" width="600px"/>
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_.jpg?raw=true" width="600px"/>
<img src = "https://github.com/takashicompany/spreadwriter/blob/master/images/build/IMG_.jpg?raw=true" width="600px"/>

-->
