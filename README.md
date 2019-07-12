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
|title|string|null|
|comments|string|null|
|id|string|null|

### Association
<!-- コメントテーブルのアソシエーション -->

## membersテーブル

|Column|Type|Options|
|name|string|-------|
|image|string|-------|
|group_id|integer|-------|

### Association
<!-- メンバーテーブルのアソシエーション -->

##  groupテーブル

|Column|Type|Options|
|name|string|-------|
|image|string|-------|
|group_id|integer|-------|

### Association
<!-- グループテーブルのアソシエーション -->

## usersテーブル

|Column|Type|Options|
|email|string|-------|
|nickname|string|-------|
|id|integer|-------|

### Association
<!-- ユーザーーテーブルのアソシエーション -->


### Association
- belongs_to :group
- belongs_to :user