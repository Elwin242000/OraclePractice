# Oracle Practice 06/07/2022

## Find Customer Referee

- SQL schema:

  ![find_customer_referee_sql_schema](../img_sql_schema/7/6_find_customer_referee_sql_schema.png)

- Example:

  ![find_customer_referee](../img_example/7/6_find_customer_referee.png)

- <ins>query:</ins>
  ```sql
  select name
  from Customer
  where nvl(referee_id,0) != 2
  ```
