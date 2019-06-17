# README

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

## userテーブル
|Column|Type|Options|
|-----|----|-------|
|name|string|null: false|
|email|string|null: false, unique: true|
|encrypted_password|string|null: false, unique: true|

### Association
- has_many :reviews

## reviewテーブル
|Column|Type|Options|
|-----|----|-------|
|review|text|
|image|text|
|mountain_id|integer|null: false, foreign_key:true|

### Association
- belongs_to :mountain
- belongs_to :user

## mountainテーブル
|Column|Type|Options|
|-----|----|-------|
|name|string|
|image_url|text|
|detail|text|

### Association
- has_many :reviews