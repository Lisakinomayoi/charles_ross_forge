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

