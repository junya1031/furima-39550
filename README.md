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

#usersテーブル
|Column-------------------|Type-------|Options--------------------------|
|nickname                 |string     |null: false                    |
|email                    |string     |null: false, unique: true      |
|password                 |string     |null: false                    |
|last-name                |string     |null: false                    |
|first-name               |string     |null: false                    |
|last-name-kana           |string     |null: false                    |
|first-name-kana          |string     |null: false                    |
|birth-date               |datetime   |null: false                    |

#itemsテーブル
|Column-------------------|Type-------|Options------------------------|
|user-id                  |references |null: false, foreign_key: true |
|item-name                |string     |null: false                    |
|item-info                |text       |null: false                    |
|item-category            |string     |null: false                    |
|item-sales-status        |string     |null: false                    |
|item-shipping-fee-status |string     |null: false                    |
|item-prefecture          |string     |null: false                    |
|item-scheduled-delivery  |integer    |null: false                    |
|item-price               |integer    |null: false                    |


#purchase-recordsテーブル
|Column-------------------|Type-------|Options------------------------|
|user-id                  |references |null: false, foreign_key: true |
|item-id                  |references |null: false, foreign_key: true |


#shipping-addresテーブル
|Column-------------------|Type-------|Options------------------------|
|purchase-record-id       |references |null: false, foreign_key: true |
|postal-code              |string     |null: false                    |
|prefecture               |string     |null: false                    |
|city                     |string     |null: false                    |
|addresses                |string     |null: false                    |
|building                 |string     |null: false                    |
|phone-number             |string     |null: false                    |
