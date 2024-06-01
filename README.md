# Botanispot
![Botanispot _logoicon_Dark](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/000be58c-8719-4704-96dc-c750b0e4b211)  

ログやBranchが複雑になるため、3つにリポジトリを分けて管理しております。  
root:[plants_demo_app_v2_root](https://github.com/sousukegit/plants_demo_app_v2_root)  
front:[plants_demo_app_v2_front](https://github.com/sousukegit/plants_demo_app_v2_front)  
back:[plants_demo_app_v2_back](https://github.com/sousukegit/plants_demo_app_v2_back)   

フロント・バックエンドではそれぞれのコミットログやブランチを管理し、  
Rootではフロント・バックエンドの最新のコミットファイルを管理しています。


## プロダクト

プロダクト名：Botanispot  
リンク：[botanispot.com](https://botanispot.com)  
概要：観葉植物に特化した店舗情報を地図上で探すことができるユーザー投稿型サービス  
アイコン:  
観葉植物と店舗の融合をイメージ  
<img width="90" alt="Botanispot_logo_dark" src="https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/aa74cc67-1c3b-4fb0-a63b-f9a8017d0008">  
※注釈  
2024年5月時点、愛媛県内の店舗データのみになっております。  

## コンセプト

__探そう、欲しい一株を実物で。__
![topberner](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/3d101023-ac5d-4917-bfd9-0fdcea65f445)

## 開発背景

私はGreenNeoSoulというブログで珍奇植物を家で楽しむ方法を発信しております。
![gns_maru_white-01](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/37fd012c-10e3-41f7-9b8a-264c8a6e392f)
リンク：[greenneosoul.com](https://greenneosoul.com)

そこの読者にアンケートをとり、ニーズとして多かった「実物を見て、安心して植物を選びたい」という声から生まれました。

こういった声の背景は一部のものではありません。
観葉植物はコロナ禍をきっかけにブームになりましたが、ネット上の情報はまだまだ少ないです。

また植物は何度も買うものではなく、比較的高価な買い物です。
そして生き物であるため状態・形も非常に大事で、気に入った株を自分の目で見たい人が多いです。

しかし、観葉植物の業界はリアル店舗中心やローカルな情報となっていることもあり、Webやネットの発信はまだまだ弱い部分がある世界です。
すばらしい店舗があるにもかかわらず、ユーザーが店舗情報までたどり着けないことが多く、フリマなどのネット通販で購入するケースが多いです。

そんな店舗とユーザーのニーズをマッチさせるため、アプリを開発しました。

## 特徴

### 地図上から近くのショップを探すことができる
地図上から近くの観葉植物のお店を探すことができます。  
また、お店の管理状態や、価格帯、マニア度など、植物目線のユーザー評価を設けております。  
お店に行く前に、規模感やなどを把握することができます。  
### お店の情報をシェアできる
ユーザー登録をすると、店舗のレビューを書き込むことができます。  
お気に入りのスポットの評価・投稿をしてみましょう  

### インスタやGoogleMAPとの違い
観葉植物が置いてある店、特化した店の情報をまとめたアプリは世の中にまだありません。

また本アプリは観葉植物に特化しており、口コミ書き込み時に独自の評価制度を設けています。

例えば、管理状態やマニア度や価格など、店舗に行く前に植物購入者が気になる情報はGoogleMAPにはありません。

また植物と言っても幅広く、お花、造園、インテリアグリーンすべて観葉植物でくくられているため、GoogleMAPだとヒットがイマイチです。

またインスタで店舗を探したりするケースもありますが、ハッシュタグから近くの店舗を探すのは情報アクセスに時間がかかります。
また店舗からの発信に依存するため、ユーザー目線でこの店舗がどうなのか、といった声が分かりにくいというデメリットがあります。

## 制作期間

約3か月です。

毎朝4：30起床して時間を確保し、コツコツ進めていきました。  
多少ムラはありましたが、平日は出社までの朝2時間＋帰宅後の1時間で約３時間、週末は4〜6時間程度行っておりました。

開発に必要な基礎知識は、それまでに業務や自己学習でで身に着けておりました。


## 技術について
### 工夫した点
* フロントエンドとバックエンドを分けたSPA開発を行い、実務と運用を意識した構成にしている。
* TailwindCSSを利用し、容易なレスポンシブ対応と柔軟なカスタマイズを可能にしている。
* Dockerを利用し、本番と開発の環境差異を減らし、軽量スケーリングできる設計にしている。
* ChartJSを利用し、植物別評価の店舗の傾向を一目で見やすいUI設計している。
* GoogleMapAPIを用いて、場所から店舗を探せるように設計する。
* Nuxt3のmiddleware、pluginsを用いて再訪問時やページ遷移時にトークンを検証する設計にしており、ログイン前&不正な情報の場合はリダイレクトされ、データにアクセスできないようになっている。
* JWTを利用し、Railsが発行したトークンでログイン時のトークン認証・セッション永続化を実現している
* Piniaを利用してストアにデータを保存し、再ロード時もデータが消えずログインした状態が保持されるようにしている。
* AWS ECSonFargeteを用いて、アプリケーション開発に集中できるようなサーバーレスの設計にしている。
* Route53、ACM、ALBを用いて、独自ドメイン＋常時SSL化を行い安全に通信している。
* CloudFrontのキャッシュを利用した静的コンテンツにアクセスさせることで、表示スピードができるだけ早くなるよう意識している。
* Rspecを用いて自動テストを行っている
* Git＋Githubを用いてソース管理し、実務を意識した開発を行っている

### つまずいたり苦労した点
* フロントエンドの環境構築  
NuxtのDockerで立ち上げた時起動やホットリロードが異常に重く、ちゃんと開発できるまでに苦労しました。  
環境を見直して、NodeModuluをバインドマウントからボリュームマウントに代えることで、開発環境の軽量化を実現できました。

* ライフサイクルを意識したフロントエンド開発  
開発初期はよく理解しないままSSRで設計しており、ハイドレーションエラーだらけになってしまいました。  
そこから、SSRやSPAの違いや Vueのライフサイクルや仮想DOMについて学び、onmountedを使用して描画のタイミングを調節したり、Nuxt3のmiddlewareやpluginなどを利用してログイン状態管理ができました。  
最終的に、本プロダクトはクライアント側で重たい処理が発生するような動的コンテンツは少ないため、SSRのためにサーバーを立てる程の必要はないと判断し、SPAに設計変更しました。  

* クエリ  
ActiveRecodeでほしいクエリが書けないときに苦労しました。  
例えば、複数カラムで平均値などの集合関数をActiveRecode単体では使用できません。  
そのため、そういった少し複雑なクエリは、SQLを書いて対応しました。  

* 画像アップロード機能  
画像アップロード機能のフロント・バックエンド機能に苦労しました。  
ActiveStorageをRailsAPIモードを用いて開発したためRailsのヘルパーが使えず、プレビュー画面やオブジェクトの受け渡しなど、ActiveStorageの仕様を理解するのに苦労しました。  
Railsガイドやブログ記事、ドキュメントを参考にしながら、複数画像のCRUD操作を実装することができました。  

* GoogleMapAPI  
GoogleMapAPIの問い合わせが増えるとどうしても表示速度が遅くなりました。  
店舗の情報をいち早く表示する必要があることと、有料APIの問い合わせ回数を減らす運用を考えました。  
結果、緯度経度はマスタデータへ、その他の情報は詳細検索時に問い合わせするようなテーブル設計に変更しました。  
総合的に見て、ユーザビリティと運用を考慮した設計にしました。

* インフラ構築全般  
AWSを利用したコンテナ環境の構築に大変苦労しました。  
AWS経験はあったものの、既存のVPCやEC2で作業することが多く、全くゼロからVPC・ネットワーク・セキュリティグ構成を作る経験はありませんでした。  
特にECS on Frageteの構築や、IAMの設定やネットワーク不具合など、上手くいかず心が折れそうになりそうなときもありました。  
参考書やネット情報をもとに障害をひとつづクリアしていきましたが、一人で考えても分からない部分は、できるエンジニアにアドバイスいただきながら、なんとかデプロイすることができました。  
アプリケーションのインフラ構成については、今後注力して知識を入れていきたい部分であります。  

* Nginxを用いたコンテナ間のソケット通信   
ページ速度の改善や開発効率のため、SSRからSPAに設計を変更し、クラウドフロント経由かつNodeを使わずNginxでプロキシを行う仕様にしました。  
ソケット通信については初めて扱う技術でしたので理解に苦労しましたが、原理を学びながらコンテナボリュームを共有する設定を行うことで実装することができました。  
Nginxを置いた理由はPumaはAppサーバーなのでユーザー直のアクセス用として設計されておらず、アクセス負荷を考慮したためです。  


### 使用技術
#### ■バックエンド
* Ruby 3.1.4
* Ruby on Rails 7.0.8
* rspec-rails 6.1.2

#### ■フロントエンド
* Vue 3.4.15
* Nuxt 3.10.1
* Tailwind Css 6.11.4
* Nginx 1.23.2

#### ■DB
* MySQL 8.0.28

#### ■開発環境
* Docker 26.0.0
* Git 2.42.0

#### ■インフラ
* Amazon Web Service
（CloudFront、S3、Route53、ACM、ALB、RDS、ECS、ECR、CloudWatch、Anthena、VPC）

　
### 技術選定
「モダンな技術であること」  
「ドキュメントや記事がしっかりしていること」  
「業務で触れていて効率的なキャッチアップになること」  
この3の理由から選びました。

#### Ruby
##### 目的
APIの開発

##### 選定理由
* Railsを含むアプリ開発に強力なGemがたくさんある  
* 日本語ドキュメントも多く、独学で困ったときに解決しやすい  
* 求人も多く、即戦力になりやすい  
* 業務で使用している言語でありキャッチアップしやすい  

#### Ruby on Rails 
##### 目的
APIを効率的に開発する

##### 選定理由
* RubyでのAPI開発をより効率化するフレームワークのため  
* Laravelと比べて、チュートリアルや日本語解説の記事がしっかりしていたため  

#### Vue 
##### 目的
フロントエンド開発

##### 選定理由
* リアクティブにデータをDOMを自動的に同期してくれる便利機能が多い  
* 再利用可能なコンポーネントを作成しやすい  
* Reactと比べてHTMLライクで直観できな記述であり、学習しやすい  
* 業務で使用している言語でありキャッチアップしやすい  

#### Nuxt 
##### 目的
フロントエンド開発の効率化

##### 選定理由
* Vueでのフロントエンド開発をより効率化するフレームワークのため  
* Vue単体で使用するときに比べて、初期設定の簡便さ、自動ルーティング、ホットリロード、pluginsやmiddlewareなど開発生産性の利点が高い

#### TailwindCss 
##### 目的
スタイル設定やレスポンシブ対応の効率化

##### 選定理由
* あらかじめまとめられたクラスが使用できる  
* レスポンシブ対応がしやすい  
* VuetifyやBootstrapに比べて自由度が高く、CSSの基礎知識があれば学習コストが低い 

#### MySQL
##### 目的
マスタデータ（ユーザー・店舗）やトランザクションデータ（レビュー）を記録するDBが必要

##### 選定理由
* 仮にバックエンドがRailsでない他のサーバーサイド言語になっても、PostgresやOracleと比べて互換性のあるデータベースである
* 業務で毎日SQLを触っていたので慣れていた

#### Nginx 
##### 目的
Railsサーバー（puma）の前段のプロキシとして、負荷分散のため使用

##### 選定理由
Apacheよりシングルスレッドのためメモリ消費が少なく、高速であるため

#### Docker 
##### 目的
本番環境での差異を軽減するため

##### 選定理由
VMwareのような仮想環境より高速であり、軽量で本番でもスケーリングしやすいこと。

#### Amazon Web Service
##### 目的
本番環境反映のため

##### 選定理由
* シェア率も高く、アプリケーションに関するインフラ知見が整っているサービスである。  
 企業で使用するインフラ知識と直結できること。   
* サービスの種類が豊富でサードパーティーとの連携も充実しているため、個人レベルでやりたいことは大体実現可能なサービスがそろっていること  
* 他のクラウドサービスより業務経験があったこともあります。  


## 実装機能
* 店舗関連  
    * GoogleMap表示機能  
    * レーダー評価機能  
    * タブによるソート機能  
    （すべて、写真のみ、口コミのみと情報を分ける）  
* レビュー関連  
    * レビュー投稿機能  
    * レビュー編集機能  
    * レビュー削除機能  
    * レビュー参照機能  
* ユーザー関連  
    * ユーザー登録機能  
    * ゲストユーザーログイン  
* その他  
    * ダークモード機能  


## 挑戦したい技術
* サードパーティーのログイン機構
* CI/CDツールによる自動デプロイ


## 制作しての感想
### アウトプットを怠ってはいけない

### フィードバックはスキルアップの近道

### 開発は大変だけど楽しい

## 参考教材












