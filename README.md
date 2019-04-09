# sql-query

***What is the meaning of the MySQL collation utf8mb4_0900_ai_ci?***

- `uft8mb4` means that each character is stored as a maximum of 4 bytes in the UTF-8 encoding scheme.
- `0900` refers to the Unicode Collation Algorithm version. (The Unicode Collation Algorithm is the method used to compare two Unicode strings that conforms to the requirements of the Unicode Standard).
- `ai` refers accent insensitivity. That is, there is no difference between e, è, é, ê and ë when sorting.
- `ci` refers to case insensitivity. This is, there is no difference between p and P when sorting.

## Cheat

### create schema

```sql
CREATE SCHEMA `{schema-name}` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci ;
```

## Reference

- https://www.monolune.com/what-is-the-utf8mb4_0900_ai_ci-collation/
