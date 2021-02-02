# README

## users テーブル

| Column             | Type    | Options     |
| ------------------ | ------- | ----------- |
| nickname           | string  | null: false |
| email              | string  | null: false |
| encrypted_password | string  | null: false |

### Association

- has_many :posts


## posts テーブル

| Column        | Type      | Options                        |
| ------------- | --------- | ------------------------------ |
| name          | string    | null: false                    |
| memo          | text      |                                |
| washlet_id    | integer   | null: false                    |
| user          | reference | null: false, foreign_key: true |
| start_time_id | integer   | null: false                    |
| end_time_id   | integer   | null: false                    |
| style_id      | integer   | null: false                    |
| quantity      | integer   | null: false                    |

### Association

- belongs_to :user



## アプリケーション名
D.toilet

## アプリケーション概要
 
自分の周辺に利用可能なトイレがあるかどうか調べることができるアプリケーションです。

 
## URL
 
## テスト用アカウント

## 利用方法
 
1. トップページにGoogleマップが表示されており、登録されているトイレの情報を確認できます。
2. トイレ情報を登録するには、ご自身の情報を登録してください。
3. ご自身の情報を登録すると、トイレの情報を編集そして削除できます。但し、ご自身の投稿したトイレの情報に限ります。
 
## 目指した課題解決
 - いざトイレに行きたくなった時、どこにトイレがあるか分からないという経験はないですか？
   少なからず私はあります。何度も。
   そんな私の経験から他にもこのような経験をされた方の手助けになるようなものを作りたいと思いました。

 
## 洗い出した用件
 - 投稿機能
 - ユーザー登録機能
 - 投稿内容編集機能
 - 投稿内容削除機能
 - GPS機能
 - GoogleMapのAPI
