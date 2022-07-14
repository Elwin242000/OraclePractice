# Oracle Practice 08/07/2022

## Not Boring Movies

- SQL schema:

  ![not_boring_movies_sql_schema](../img_sql_schema/7/8_not_boring_movies_sql_schema.png)

- Example:

  ![not_boring_movies](../img_example/7/8_not_boring_movies.png)

- <ins>query:</ins>

  ```sql
  select *
  from Cinema
  where mod(id,2) = 1
    and description not like 'boring'
  order by rating desc
  ```
