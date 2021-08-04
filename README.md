# テーブル設計

## categories テーブル

| Column           | Type   | Options     |
| -----------------| ------ | ----------- |
| id               | bigint | ----------- |
| name             | string | unique:true |

### Association
- belongs_to :idea

## ideas テーブル

| Column           | Type   | Options      |
| -----------------| ------ | -----------  |
| id               | bigint | -----------  |
| category_id:     | bigint | null: false, foreign_key: true |
| body             | text   | null: false  |

### Association
has_many :categories
