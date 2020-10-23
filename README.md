## userテーブル

| Column    | Type       | Options                        |
| --------- | ---------- | ------------------------------ |
| name      | string     | null: false, foreign_key: true |
| email     | string     | null: false, foreign_key: true |
| password  | string     | null: false, foreign_key: true |

### Association
- belongs_to :home

## homeテーブル

| Column         | Type        | Options                        |
| -------------- | ----------- | ------------------------------ |
| user_id        | references  | null: false, foreign_key: true |
| log_id         | references  | null: false, foreign_key: true |
| prefecture_id  | integer     | null: false, foreign_key: true |

### Association
- belongs_to :user
- has_many :logs


## logテーブル

| Column        | Type           | Options                        |
| ------------- | -------------- | ------------------------------ |
| image         | references     | null: false, foreign_key: true |
| place         | string         | null: false, foreign_key: true |
| text          | string         | null: false, foreign_key: true |
| prefecture_id | integer        | null: false, foreign_key: true |

### Association
- belongs_to :home

