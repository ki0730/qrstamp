# QR角印とは？

> WHAT IS "QR Stamp" ?
>
> "QR Stamp" is a digital seal designed as an alternative to Japanese so called "square stamps".

株式会社鉄飛テクノロジー QR角印について（https://www.teppi.com/column/misc/qrstamp_about） 

## QR角印は電子印鑑です

- 日本の企業間取引において書類の正当性を表明する「認印」として広く使われる、
- いわゆる「角印」の代替となるべく開発された、電子印鑑です
  - 電子印鑑システム全体、あるいはシステムによって生成された印影を意味します



## 角印の代わりに使えます

中心のQRコードを組織名で囲み、従来の角印に似通った、同じサイズ（約21mm四方）のデザインです。

- 印影の中央にQRコードを持つことが外見上の特徴ですが
- 人の目で見ても、社名が一目瞭然で、角印の代わりに運用できます
- 一定の役職者のみが印影をその都度生成し、生成された画像ファイルを文書中に貼り込んで使います
- 印影は生成のたびに毎回異なるユニークなQRコードを含みます



## 書類に一定の信頼性を付加します

- 中心のQRコードが、有効なURLとして捺印情報Webページへのリンクとなっています。

- スマホやタブレットでQRコードを読み取れば、捺印情報ページで書類の信頼性を監査できます。

- 以下のような観点から書類の監査が可能です

  - 捺印情報ページが有効であるかどうか？

  - 捺印情報ページのドメインは書類の発行者が所有するインターネットドメインかどうか？

  - 捺印情報の内容（日付時刻・組織名やコメントなど）が書類の内容と矛盾しないかどうか

    

![image-20200416175237167](docs/assets/README/image-20200416175237167.png)

## 考案の動機

QR角印の位置づけと考案の狙いについては、下記文書で説明しています。

#### QR角印考案の動機 [00_MOTIVATION.md](./docs/00_MOTIVATION.md)

- 「電子印鑑」といわれるもににはいくつかの種類がありますが
  - QR角印は、従来の「角印」の代わりに、紙に印刷されて文書として流通させることを前提に設計されたものです。
    - 実印と印鑑証明の代わりとなったり、契約書の署名捺印の代わりになるような、電子署名・電子証明書システムとは、全く異なり、相対的に低コストで手軽なものです。
    - 紙媒体での流通・保存が可能であり、既存取引先との「従来通りの紙文書ワークフローを乱さない」特性を持ちつつ、「従来の角印と同等以上の信頼性」を有します。
    - 捺印作業の省略を実現できることで、大幅な省力化が期待できます。



## デモサイト

https://qrsample.teppi.net/



## 運用イメージと効果

### 想定されるシステム全体像

- QR角印システム

  - QR角印の印影画像を生成します

  - 同時に、捺印情報ページをインターネットに公開します

    （印影画像に含まれるQRコードは捺印情報ページのURLです）

- 帳票作成ツール・帳票作成システム

  - 例えば、請求書作成や見積書作成システムなどの帳票作成システムから、QR角印システムを呼び出して、生成されたQR角印の印影を含む帳票PDFファイルを生成することを想定します。
  - あるいは、手動で生成したQR角印を、Microsoft Office(ExcelやWordなど）作成した帳票に貼り付けて、そこから印刷あるいはPDF出力して運用することも可能です。



## 導入について

※ ここではQR角印システムの最低限の導入に必要な要素について記します

（帳票作成システムや文書作成ツールについては別途ツールの利用や、システム開発が必要ですが、それは本文書の範囲外です。）

### 前提となるシステム

QR角印（生成＆捺印情報公開）システムは

- Linux

- node

  で動きます

詳しくは

**インストール・設定手順** [20_HOW_TO_DEPLOY.md](./docs/20_HOW_TO_DEPLOY.md) 

**AWS EC2への導入例** [30_AWS_EC2_DEPLOYMENT.md](./docs/30_AWS_EC2_DEPLOYMENT.md)

をご覧下さい





## 関連文書

#### QR角印考案の動機 [00_MOTIVATION.md](./docs/00_MOTIVATION.md)

​	QR角印の位置づけと考案の狙いについて記述しています

#### QR角印標準 [10_QR_STAMP_STANDARDS.md](./docs/10_QR_STAMP_STANDARDS.md)

#### インストール・設定手順 [20_HOW_TO_DEPLOY.md](./docs/20_HOW_TO_DEPLOY.md)

#### AWS EC2への導入例 [30_AWS_EC2_DEPLOYMENT.md](./docs/30_AWS_EC2_DEPLOYMENT.md)



