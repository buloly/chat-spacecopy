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

## commentsテーブル

|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
<!-- コメントテーブルのアソシエーション -->

## membersテーブル

|Column|Type|Options|
|name|string|-------|
|image|string|-------|
|group_id|integer|-------|

### Association
- belongs_to :user

<!-- メンバーテーブルのアソシエーション -->

##  groupsテーブル

|Column|Type|Options|
|name|string|-------|
|image|string|-------|
|group_id|integer|-------|

### Association
- belongs_to :user
- belongs_to :member
<!-- グループテーブルのアソシエーション -->

## usersテーブル

|Column|Type|Options|
|email|string|-------|
|nickname|string|-------|
|id|integer|-------|

### Association
- has_many :comments
<!-- ユーザーーテーブルのアソシエーション -->





### Association
- belongs_to :group
- belongs_to :user