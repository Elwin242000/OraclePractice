# Oracle Practice 05/07/2022

## The Latest Login in 2020

- SQL schema:

  ![the_lastest_login_in_2020_sql_schema](../img_sql_schema/7/5_the_lastest_login_in_2020_sql_schema.png)

- Example:

  ![the_lastest_login_in_2020](../img_example/7/5_the_lastest_login_in_2020.png)

- <ins>query:</ins>
  ```sql
  select
    user_id,
    max(time_stamp) last_stamp
  from Logins
  where to_char(time_stamp,'yyyy') = 2020
  group by user_id
  ```
