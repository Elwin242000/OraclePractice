# Oracle Practice 06/07/2022

## Fix Names in a Table

- SQL schema:

  ![fix_names_in_a_table_sql_schema](../img_sql_schema/7/6_fix_names_in_a_table_sql_schema.png)

- Example:

  ![fix_names_in_a_table](../img_example/7/6_fix_names_in_a_table.png)

- <ins>query:</ins>
  ```sql
  select user_id, initcap(name) name
  from Users
  order by user_id
  ```
