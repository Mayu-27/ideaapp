# テーブル設計

## categories テーブル

| Column           | Type   | Options     |
| ———————————————— | —————— | ——————————— |
| name             | string | unique:true |

### Association
- belongs_to :idea

## ideas テーブル

| Column           | Type       | Options      |
| ———————————————— | —————————— | ———————————— |
| category_id      | references | null: false, foreign_key: true |
| body             | text       | null: false  |

### Association
has_many :categories
