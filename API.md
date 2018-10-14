# README

#DB設計

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false |
|sex|integer|null: false |
|age|integer|null: false |
|email|string|null: false, foreign_key: true|
|pasword|integer|null: false, foreign_key: true|
|password_comfirmation|integer|null: false, foreign_key: true|
|message_id|integer|null: false, foreign_key: true|

### Association
- has_many :message
- has_many :location

## locationsテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user


## profilesテーブル

|Column|Type|Options|
|------|----|-------|
|comntent|text|null: false |
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user


## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|null: false, foreign_key: true|
|image|string|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group




## 仕様メモ

- ログイン

マリンチャットは、email,passwordとかない。
ログインはどうするか？

マッチアプリに、本アカ使いたくないから、サブアドレス、パスワードを入れると、パスワーをを忘れてログインできなくなる人いそう。

→ 
passwordわからなくなった人にメアド入力でパスワード教えるかリセットする。

- ログインの使用
email,
password
 
- deveise利用



