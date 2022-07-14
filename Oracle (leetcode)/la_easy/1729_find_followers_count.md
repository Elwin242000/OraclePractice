# Oracle Practice 07/07/2022

## Find Followers Count

- SQL schema:

  ![find_followers_count_sql_schema](../img_sql_schema/7/7_find_followers_count_sql_schema.png)

- Example:

  ![find_followers_count](../img_example/7/7_find_followers_count.png)

- <ins>query:</ins>
  ```sql
  select
    user_id,
    count(*) as followers_count
  from Followers
  group by user_id
  order by user_id
  ```
