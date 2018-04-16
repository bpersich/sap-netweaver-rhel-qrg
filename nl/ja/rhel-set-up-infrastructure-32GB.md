---



copyright:
  years: 2018
lastupdated: "2018-02-26"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 1. 32 GB サーバーの注文
{: #install_32GB}

## サーバーの注文
{: #order_32GB}

1. お客様固有の資格情報を使用して、[{{site.data.keyword.cloud_notm}}インフラストラクチャーのカスタマー・ポータル](https://control.softlayer.com)にログインします。
2. 「アカウント要約」ページで**「デバイス」**をクリックします。
3. 「デバイス」ページの「{{site.data.keyword.baremetal_short}}」で**「月単位」**をクリックします。「サーバー・リスト」ダイアログ・ボックスが表示されます。
4. **「月単位の開始価格 (STARTING PRICE PER MONTH)」**の下のハイパーリンクをクリックして、サーバー **「BI.S1.NW32 (OS Options)」**を選択します。

## サーバー・オプションの選択
{: #options_32GB}

1. **「数量」**フィールドは**「1」**のままにしておきます。
2. **「データ・センター」**には**「TOR01」**を選択します。データ・センターのリストは、特定のデータ・センターにおける製品の可用性によって異なります。
3. **「サーバー」**は、デフォルトでお客様の選択に基づいた事前定義値になるため、変更することはできません。
4. **「RAM」**の選択項目は、デフォルトでお客様のサーバーの選択に基づいた事前定義値になり、変更できませんが、**「32 GB RAM」**をクリックします。
5. **「オペレーティング・システム」**として、**「Red Hat Enterprise Linux for SAP Business Application 6.X」**を選択します。
6. **「ハード・ディスク」**では、2 番目の 2 TB SATA ディスクを選択し、両方のディスクから、合計ストレージ量をカバーする RAID ストレージ・グループ RAID1 を作成して、**「パーティション・テンプレート」**として**「Linux 基本」**を選択します。**「LVM」**はチェック・マークを外したままにします。
7. **「パブリック処理能力」**には**「500 GB」**を選択します。
8.	**「アップリンク・ポート速度」**には**「1 Gbps 冗長パブリックおよびプライベート・ネットワーク・アップリンク」**を選択します。
9. 他のフィールドはすべて、デフォルト値のままにします。オプションの詳しい説明については、[ベア・メタル・サーバーの構成](https://console.bluemix.net/docs/bare-metal/configuring.html#setting-up-your-bare-metal-servers)を参照してください。
10.	ページ下部の**「注文に追加」**をクリックします。注文を確認すると、「ご精算」ページにリダイレクトされます。

## 「拡張システム構成」のセットアップ
{: #adv_config}

「拡張システム構成」の各フィールドには、表 1 の値を使用します。詳細は、[拡張システム構成](https://console.bluemix.net/docs/bare-metal/configuring.html#advanced-system-configuration)のガイドラインに記載されています。

1. スクロールダウンして、**「拡張システム構成」**で表 1 の値を入力します。

|              フィールド          |      値                                                              |
| -------------------------------- | -------------------------------------------------------------------- |
|バックエンド VLAN                 | ドロップダウン・リストから選択。例: `tor01.bcr01a.1241`|
|サブネット                        | ドロップダウン・リストから選択。例: `10.114.63.64/26`  |
|フロントエンド VLAN               | ドロップダウン・リストから選択。例: `tor01.fcr01a.1199`|
|サブネット                        | ドロップダウン・リストから選択。例: `169.55.137.160/27`|
|プロビジョン・スクリプト          | デフォルトは「なし」                                                 |
|SSH 鍵                            | 追加する                                                             |
|ホスト名                          | 例: `e2e1270`                                       |
|ドメイン                          | 例: `saptest.com`                                   |
{: caption="表 1. 32 GB 拡張構成の値" caption-side="top"}  

## 選択内容の確認
{: #confirm_selections}

1. 「ご精算」ページの選択内容を確認して、ページの右側の**「クラウド・サービスのご利用条件」**および**「サード・パーティーのソフトウェアのご使用条件」**をクリックします。
2. フォームの右側の**「注文の送信」**をクリックします。注文番号を示すページにリダイレクトされます。このページは注文の受領証でもあるので、印刷できます。さらに、件名が*「お客様の IBM Cloud 注文 ## は承認されました」*という確認の E メールも受け取ります。## は、お客様のご注文番号です。

ご注文の送信後、お客様のサーバーは、ご注文に応じて 1 時間から 4 時間のうちに使用できるようになります。プロビジョニング・ステップの状況については、カスタマー・ポータルのメイン・ページ (**「デバイス」>「デバイス・リスト」**) の「デバイスの詳細」画面で確認できます。お客様の所定のホスト名とドメインに一致する**「デバイス名」**をクリックして、デバイスの状況を確認してください。

## 次のステップ
 
  [2. SAP インストール用のサーバーの準備](/docs/infrastructure/sap-netweaver-rhel-qrg/rhel-prepare-server-32GB.html)
  
  [3. パーティショニングとファイル・システム](/docs/infrastructure/sap-netweaver-rhel-qrg/rhel-partition-32GB.html)