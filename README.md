# READ ME

## RISC!!  

![スクリーンショット 2020-07-22 19 54 08](https://user-images.githubusercontent.com/58941838/88168272-25ff5b80-cc55-11ea-9300-95aba297d201.png)

### URLは[こちら](hhttps://www.risc.website/ )

### サービスの説明  
全てのサイクリストが安全にサイクリングできるように危険箇所をシェアするサービスです。  
ユーザーが自転車で走行する上で危険な箇所をGoogle Map上にマーカーを表示および内容を見ることができます。</br>

![Post_Show](https://user-images.githubusercontent.com/58941838/88167260-8097b800-cc53-11ea-9570-dc279ee7092c.gif)

ユーザー登録をしていただけると、危険箇所を登録していただけます。</br>
また登録だけではなく、他ユーザー投稿へのコメント、役に立った評価、ブックマーク保存機能が使用できます。
![New_post](https://user-images.githubusercontent.com/58941838/88168150-f81a1700-cc54-11ea-8662-cee95392379d.gif)  


## 開発について  
このサービスは現在私が個人で開発しております。  
### 1. 開発環境は以下となります。</br>
  
  | 名前 | バージョン |
  ----|---- 
  | OS | macOS Catalina |
  | Ruby | 2.5.3 |
  | Rails | 5.2.4.3|
  | SQL | MySQL 5.2.7.9 |
  | Editor | Vim |  
  
  使用技術：HTML/CSS/Bootstrap/JavaScript/jQuery/Ruby/Ruby on Rails/MySQL/AWS(EC2にデプロイ)

### 2. データベース図  
データベース図は下記です。
![messageImage_1595413157640](https://user-images.githubusercontent.com/58941838/88165664-036b4380-cc51-11ea-98b0-9908d273161a.jpg)  

### 3. 本番環境について  
AWSを用いてデプロイしました。インフラ構成図はこちらです。
![インフラ](https://user-images.githubusercontent.com/58941838/88173590-cbb6c880-cc5d-11ea-9fd2-d19d24cb94da.png)  

## 開発で意識した点
1. Google Map APIを用いるだけではなく、ユーザーがマップ上でクリックした箇所にマーカーを置き、  
保存時にはマーカーの緯度・経度が保存されるようにしている点です。

2. データベース設計時に正規化し、細かくテーブルを分けた上で、  
データを登録する際には同時に親子関係にあるモデルを同時保存できるようした点です。

3. ユーザーが使う状況(電波が弱い可能性等)を想定し、過度な装飾を避け、シンプルなデザインにした点です。

## 課題やこれから実装したい機能など  
### 課題点(2020年7月時点)  
1. HTTPS化していない点  (2020年7月23日改善済)
2. 独自ドメインを使用していない点 (2020年7月23日改善済)
3. テストコードが不十分な点  
4. 投稿を削除するとき、確認ダイアログが実装されていない点 (2020年7月28日改善済)
### 実装したい機能  
1. 多言語サイト化
2. 危険箇所の条件フィルター機能の実装
3. 画像投稿機能  
4. Ruby,Railsのバージョンアップ
