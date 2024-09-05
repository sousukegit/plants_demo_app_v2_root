# アプリ紹介

ログやブランチが複雑になるため、rootを配下に、  
3つにリポジトリを分けて管理しております。  
root:[plants_demo_app_v2_root](https://github.com/sousukegit/plants_demo_app_v2_root)  
┣front:[plants_demo_app_v2_front](https://github.com/sousukegit/plants_demo_app_v2_front)  
┣back:[plants_demo_app_v2_back](https://github.com/sousukegit/plants_demo_app_v2_back)   
┗nginx:[plants_demo_app_v2_nginx](https://github.com/sousukegit/plants_demo_app_nginx) 

フロントエンド・バックエンドではそれぞれのコミットログやブランチを管理し、  
Rootではそれぞれの最新のコミットファイルを管理しています。

## 作成したアプリ

プロダクト名：Botanispot  
リンク：[botanispot.com](https://botanispot.com)  
概要：観葉植物に特化した店舗情報を地図上で探すことができるユーザー投稿型サービス  

※注釈  
2024年5月時点、愛媛県内の店舗データのみになっております。  

アイコン:  
観葉植物と店舗の融合をイメージ  
![Botanispot _logoicon_Dark](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/000be58c-8719-4704-96dc-c750b0e4b211)  

コンセプト:  
__探そう、欲しい一株を実物で。__  
![topberner](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/3d101023-ac5d-4917-bfd9-0fdcea65f445)  

制作期間:約3か月(平日3時間、土日4-6時間)  
平日：朝4時半に起きて会社までの2時間、帰ってから1時間  
土日祝：4-6時間程度  

## アプリケーション全体のイメージ
![アプリ概要3倍v2](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/20f5a873-31ba-4e74-be3c-069338046aca)  
ログインし、店舗を探して観葉植物に特化した情報を参照できます。  
一店舗に一回のみ、ユーザーが口コミを投稿できます。  

## 開発背景
GreenNeoSoulというブログで珍奇植物を家で楽しむ方法を4年前から発信しております。  
リンク：[greenneosoul.com](https://greenneosoul.com)
![2208_gns_logo_kettei-03](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/d7d53db4-6c44-40df-b19c-736493a6d9bb)  
そこの読者にアンケートをとり、ニーズとして多かった「実物を見て、安心して植物を選びたい」という声から生まれました。  

観葉植物業界はまだまだWeb上の発信が弱く、ネット上の情報が少ないです。  

すばらしい店舗があるにもかかわらず、ユーザーが店舗情報までたどり着けないことが多く、フリマなどのネット通販で高額購入するケースが多いです。  

店舗とユーザーのニーズをマッチさせるため、アプリを開発しました。  

## 実装機能一覧
### TOP  
![機能　TOP](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/fc228d67-30b2-43d3-8d96-08d9fc1872e1)  

TOPページにどんなアプリか一目でわかるようイメージ画像を中心に記載しています  
### 店舗MAP  
![機能　MAP２](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/5ca2857a-138c-4bc8-8808-15b3a3ec4e56)  
マーカーをタップすると地図情報から近くの店舗情報を確認できます。  

### 店舗情報タブ分け  
![機能　タブ](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/9a4b00ae-55d6-4d45-abec-7e4357ea25f3)  
すべての情報、写真一覧、口コミ一覧を直観的に切り替えれるようタブで切り分け。  
ユーザーが見たい情報にすぐアクセスできるようにしました。
### 口コミCRUD機能  
![機能　CRUD](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/1a4bb545-59af-4fb1-a974-d7387272a715)  
ユーザーが訪れた店舗を評価できます。  
加えて植物管理状態・価格・マニア度・種類など、観葉植物に特化した内容で情報精度を高めます。  

### ゲストユーザーログイン  
![機能　ゲストログイン](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/d9f9ab89-f5b5-43bb-a66f-c77cd51f9532)  
まずは使っていただくため、TOP中央にゲストログインを配置。  
通常ログインも実装済みです。  
### ダークモード機能  
![機能　ダーク](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/0b6acac4-2ab2-4c16-9703-99c46b8d6f37)  
暗い場所でも使いやすいようダーク切り替えボタンを搭載。  
再訪問後も保たれるようCookieでブラウザ上に状態を保存。  

## システム構成図
![AWS](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/02d97cf7-c3e5-4cca-8b64-918966661e3a)  

## ER図
![ER](https://github.com/sousukegit/plants_demo_app_v2_root/assets/135125480/f255fc4c-b3c8-4f43-b47d-311fba407f1e)  

## 使用技術
### ■バックエンド
* Ruby 3.1.4
* Ruby on Rails 7.0.8
* rspec-rails 6.1.2

### ■フロントエンド
* Vue 3.4.15
* Nuxt 3.10.1
* Tailwind Css 6.11.4
* Nginx 1.23.2

### ■DB
* MySQL 8.0.28

### ■開発環境
* Docker 26.0.0
* Git 2.42.0

### ■インフラ
* Amazon Web Service
    * CloudFront
    * S3
    * Route53
    * ACM
    * ALB
    * RDS
    * ECS
    * ECR
    * CloudWatch
    * Anthena

　
## 技術選定
「モダンな技術であること」  
「ドキュメントや記事がしっかりしていること」  
「業務で触れていて効率的なキャッチアップになること」  
この3の理由から選びました。

### Ruby/Ruby on Rails 

* Railsを含むアプリ開発に強力なGemがたくさんある  
* 日本語ドキュメントも多く、独学で困ったときに解決しやすい  
* Laravelと比べて、チュートリアルや日本語解説の記事がしっかりしていたため  

### Vue/Nuxt 

* Reactと比べてHTMLライクで直観的な記述であり、学習しやすい  
* 小規模であれば双方向バインディングがコンポーネントを作るときにわかりやすい  
* Vue単体で使用するときに比べて便利機能が多く、開発生産性の利点が高い  
（自動ルーティング、ホットリロード、pluginsやmiddlewareなど）  

### TailwindCss 

* レスポンシブなどの使用頻度の高いクラスがまとまっており、かつ直観的に記述できる  
* VuetifyやBootstrapに比べて応用が利き、CSSの基礎知識があれば学習コストが低い  

### MySQL

* 仮にバックエンドがRailsでない他のサーバーサイド言語になっても、PostgresやOracleと比べて互換性のあるデータベースである  

### Nginx 

* Railsサーバー（puma）の前段のプロキシとして、負荷分散のため使用  
* Apacheよりシングルスレッドのためメモリ消費が少なく、高速であるため  

### Docker 

* 開発と本番の差異をできるだけ減らし、アプリケーション開発に集中したい。  
* 軽量で高速であり、本番でもスケーリングしやすい。  
* kubernetesより学習コストが低い。  

### Amazon Web Service  

* シェア率も高く、アプリケーションに関するインフラ知見が整っているサービスであること。  
* 企業の採用率が高く、現場で使用されているインフラ知識を深めることができること。  
* AzureやGCPと比べ、サービスの種類が豊富でサードパーティーとの連携も充実しているため、アプリ開発・運用に必要なサービスがそろっていること  














