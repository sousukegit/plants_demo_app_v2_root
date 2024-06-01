# ポートフォリオ紹介

ログやBranchが複雑になるため、3つにリポジトリを分けて管理しております。  
root:[plants_demo_app_v2_root](https://github.com/sousukegit/plants_demo_app_v2_root)  
front:[plants_demo_app_v2_front](https://github.com/sousukegit/plants_demo_app_v2_front)  
back:[plants_demo_app_v2_back](https://github.com/sousukegit/plants_demo_app_v2_back)   

フロント・バックエンドではそれぞれのコミットログやブランチを管理し、  
Rootではフロント・バックエンドの最新のコミットファイルを管理しています。

## ポートフォリオ

プロダクト名：Botanispot  
リンク：[botanispot.com](https://botanispot.com)  
概要：観葉植物に特化した店舗情報を地図上で探すことができるユーザー投稿型サービス  
アイコン:  
観葉植物と店舗の融合をイメージ  
![Botanispot _logoicon_Dark](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/000be58c-8719-4704-96dc-c750b0e4b211)  
※注釈  
2024年5月時点、愛媛県内の店舗データのみになっております。  
コンセプト:  
__探そう、欲しい一株を実物で。__  
![topberner](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/3d101023-ac5d-4917-bfd9-0fdcea65f445)  
制作期間:約3か月(平日3時間、土日4-6時間)


##  アプリケーションのイメージ

## 開発背景

私現在個人事業としてGreenNeoSoulというブログで珍奇植物を家で楽しむ方法を4年前から発信しております。  
リンク：[greenneosoul.com](https://greenneosoul.com)

そこの読者にアンケートをとり、ニーズとして多かった「実物を見て、安心して植物を選びたい」という声から生まれました。

観葉植物業界はまだまだWeb上の発信が弱く、ネット上の情報が少ないです。
すばらしい店舗があるにもかかわらず、ユーザーが店舗情報までたどり着けないことが多く、フリマなどのネット通販で購入するケースが多いです。

そんな店舗とユーザーのニーズをマッチさせるため、アプリを開発しました。
### システム構成図

###　ER図
![table_ER](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/17f553d7-f9bd-495a-adf8-ac48eaf02941)

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

* Railsを含むアプリ開発に強力なGemがたくさんある  
* 日本語ドキュメントも多く、独学で困ったときに解決しやすい  
* 求人も多く、即戦力になりやすい  
* 業務で使用している言語でありキャッチアップしやすい  

#### Ruby on Rails 

##### 選定理由
* RubyでのAPI開発をより効率化するフレームワークのため  
* Laravelと比べて、チュートリアルや日本語解説の記事がしっかりしていたため  

#### Vue 

##### 選定理由
* リアクティブにデータをDOMを自動的に同期してくれる便利機能が多い  
* 再利用可能なコンポーネントを作成しやすい  
* Reactと比べてHTMLライクで直観できな記述であり、学習しやすい  
* 業務で使用している言語でありキャッチアップしやすい  

#### Nuxt 

##### 選定理由
* Vueでのフロントエンド開発をより効率化するフレームワークのため  
* Vue単体で使用するときに比べて、初期設定の簡便さ、自動ルーティング、ホットリロード、pluginsやmiddlewareなど開発生産性の利点が高い

#### TailwindCss 

##### 選定理由
* あらかじめまとめられたクラスが使用できる  
* レスポンシブ対応がしやすい  
* VuetifyやBootstrapに比べて自由度が高く、CSSの基礎知識があれば学習コストが低い 

#### MySQL

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

##### 選定理由
* シェア率も高く、アプリケーションに関するインフラ知見が整っているサービスである。  
 企業で使用するインフラ知識と直結できること。   
* サービスの種類が豊富でサードパーティーとの連携も充実しているため、個人レベルでやりたいことは大体実現可能なサービスがそろっていること  
* 他のクラウドサービスより業務経験があったこともあります。  


## 実装機能一覧
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

## 詳細をまとめたブログ記事
リンク：[sousuke-neosoul.com](https://sousuke-neosoul.com/sousuke_portfolio_botanispot/)













