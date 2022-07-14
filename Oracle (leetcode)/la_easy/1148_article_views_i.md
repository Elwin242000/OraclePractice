# Oracle Practice 08/07/2022

## Article Views I

- SQL schema:

  ![article_views_i_sql_schema](../img_sql_schema/7/8_reformat_department_table_sql_schema.png)

- Example:

  ![article_views_i](../img_example/7/8_reformat_department_table.png)

- <ins>query:</ins>
  ```sql
  select distinct author_id as id
  from Views
  where author_id = viewer_id
  order by author_id asc
  ```
