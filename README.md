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
|image|text|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

<!-- コメントテーブルのアソシエーション -->
### Association
- belongs_to :user
- belongs_to :group




## membersテーブル

|Column|Type|Options|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

<!-- メンバーテーブルのアソシエーション -->
### Association
- belongs_to :user
- belongs_to :group
user -- members -- group



##  groupsテーブル

|Column|Type|Options|
|name|string|null: false|

<!-- グループテーブルのアソシエーション -->
### Association
- has_many :users, through: :members
- has_many :comments
- has_many :members





## usersテーブル

|Column|Type|Options|
|email|string| null: false, unique: true|
|nickname|string|null: false|

<!-- ユーザーーテーブルのアソシエーション -->
### Association
- has_many :comments
- has_many :members
- has_many :groups, through: :members







