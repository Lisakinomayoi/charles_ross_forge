# README

## users table
| Column                | Type   | Options                   |
|---------------------- | ------ | ------------------------- | 
| first_name            | string | null: false               |
| last_name             | string | null: false               |
| email                 | string | null: false, unique: true |
| password              | string | null: false               |
| password_confirmation | string | null: false               |


## Association
- has_many :blogs
- has_many :orders

## blogs table
| Column  | Type       | Options                        | 
| ------- | ---------- | ------------------------------ |
| title   | string     | null: false                    |
| date    | date       | null: false                    |
| context | integer    | null: false                    |
| user    | references | null: false, foreign_key: true |

## Assoication
- belongs_to :user

## orders table
| Column        | Type       | Options                        |
| ------------- | ---------- | ------------------------------ | 
| postal_code   | string     | null: false                    |
| prefecture_id | integer    | null: false                    |
| city          | string     | null: false                    |
| address       | string     | null: false                    |
| building      | string     |                                |
| phone_number  | string     | null: false                    |
| user          | references | null: false, foreign_key: true |

## Association
-belongs_to :user

## inquiry table
| Column  | Type      | Options     | 
| ------- | --------- | ----------- |
| first_name | string | null: false |
| last_name  | string | null: false |
| email      | string | null: false |
| message    | text   | null: false |