# Oracle Practice 08/07/2022

## User Activity for the Past 30 Days I

- SQL schema:

  ![users_activity_for_the_past_30_days_i_sql_schema](../img_sql_schema/7/8_users_activity_for_the_past_30_days_i_sql_schema.png)

- Example:

  ![users_activity_for_the_past_30_days_i](../img_example/7/8_users_activity_for_the_past_30_days_i.png)

- <ins>query:</ins>

  ```sql
  select
    to_char(activity_date,'yyyy-mm-dd') as day,
    count(distinct user_id) as active_users
  from Activity
  where activity_date between '2019-06-28' and '2019-07-27'
  group by activity_date
  ```
