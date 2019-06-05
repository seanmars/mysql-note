# sql-query

***What is the meaning of the MySQL collation utf8mb4_0900_ai_ci?***

- `uft8mb4` means that each character is stored as a maximum of 4 bytes in the UTF-8 encoding scheme.
- `0900` refers to the Unicode Collation Algorithm version. (The Unicode Collation Algorithm is the method used to compare two Unicode strings that conforms to the requirements of the Unicode Standard).
- `ai` refers accent insensitivity. That is, there is no difference between e, è, é, ê and ë when sorting.
- `ci` refers to case insensitivity. This is, there is no difference between p and P when sorting.

## Cheat

### Create schema

```sql
CREATE SCHEMA `{schema-name}` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci ;
```

### Update multiple rows at once

| id   | height | weight |
| ---- | ------ | ------ |
| 1    | 168    | 60     |
| 2    | 170    | 90     |
| 3    | 158    | 43     |
| 4    | 166    | 40     |

```sql
UPDATE person p
INNER JOIN (
    SELECT 1 AS `id`, 169 AS `height`, 66 AS `weight`
    UNION ALL SELECT 2 AS `id`, 171 AS `height`, 80 AS `weight`
    UNION ALL SELECT 3 AS `id`, 158 AS `height`, 46 AS `weight`
    UNION ALL SELECT 4 AS `id`, 169 AS `height`, 40 AS `weight`
) AS tempTable
ON s.`id` = tempTable.`id`
SET p.`height` = tempTable.`height`, p.`weight` = tempTable.`weight`;
```

## Reference

- https://www.monolune.com/what-is-the-utf8mb4_0900_ai_ci-collation/
- https://tableplus.io/blog/2018/11/how-to-update-multiple-rows-at-once-in-mysql.html
