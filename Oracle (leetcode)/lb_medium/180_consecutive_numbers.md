# Oracle Practice 24/06/2022

## Consecutive Numbers

- SQL schema:

  ![consecutive_numbers_sql_schema](../img_sql_schema/6/24_consecutive_numbers_sql_schema.png)

- Example:

  ![consecutive_numbers](../img_example/6/24_consecutive_numbers.png)

- <ins>query:</ins>
  ```sql
  select
    distinct a.Num as ConsecutiveNums
  from
  (
    select
      Id,
      Num,
      lead(ID, 2, -1) OVER (PARTITION BY Num ORDER BY id) AS id2
    from Logs
  ) a
  where a.id2 = a.id + 2
  ```
