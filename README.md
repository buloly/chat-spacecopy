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
|text|text|-------|
|user_id|integer|-------|


### Association
- belongs_to :user


<!-- コメントテーブルのアソシエーション -->

## membersテーブル

|Column|Type|Options|
|user_id|integer|-------|
|group_id|integer|-------|

### Association
- belongs_to :user
- belongs_to :group
user -- members -- group


<!-- メンバーテーブルのアソシエーション -->

##  groupsテーブル

|Column|Type|Options|
|name|string|-------|


### Association
- has_many_ :users


<!-- グループテーブルのアソシエーション -->

## usersテーブル

|Column|Type|Options|
|email|string|-------|
|nickname|string|-------|
|id|integer|-------|

### Association
- has_many :comments
- has_many :members
- has_many :users
<!-- ユーザーーテーブルのアソシエーション -->





