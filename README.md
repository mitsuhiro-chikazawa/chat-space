# README

# アプリ名



# 概要



# 本番環境

url
# ログイン情報（テスト用）
- Eメール：
- パスワード：


# 制作背景（意図）

- 
- 
- 
- 


# DEMO

# 各ビューの画像

- 
- 
- 
- 


# 工夫したポイント

- 
- 
- 
- 


# 使用技術（開発環境）

## バックエンド
## フロントエンド
## データベース
## インフラ
## Webサーバ（本番環境）
## アプリケーションサーバ（本番環境）
## ソース管理
## テスト
## エディタ


# 課題や今後実装したい機能

- 
- 
- 
- 

#Chat_Space DB設計
## usersテーブル

|Colum|Type|Options|
|------|----|------|
|name|string|null: false|
|email|string|null: false, unique: true|
|password|string|null: false, unique: true|

## Association
- has_many :messages
- has_many :users_groups
- has_many  :groups,  through:  :users_groups

## messagesテーブル

|Colum|Type|Options|
|------|----|------|
|body|text||
|image|string||
|user_id|integer|foreign_key: true|
|group_id|integer|foreign_key: true|

## Association
- belongs_to :user
- belongs_to :group


## groupsテーブル

|Colum|Type|Options|
|------|----|------|
|name|string|null: false|

## Association
- has_many :messages
- has_many :users_groups
- has_many  :users,  through:  :users_groups

## users_groupsテーブル

|Colum|Type|Options|
|------|----|------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

## Association
- belongs_to :user
- belongs_to :group

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
