# README

## userテーブル

|Column|Type|Options|
|------|----|-------|
|name |string |null: false|
|email|string |null: false|

### Association
- has_many :groups, throuh member


## groupテーブル

|Column|Type|Options|
|------|----|-------|
|name|string |null: false|

### Association
- has_many :users, through member


## membersテーブル

|Column|Type|Options|
|------|----|-------|
|user_i d|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
