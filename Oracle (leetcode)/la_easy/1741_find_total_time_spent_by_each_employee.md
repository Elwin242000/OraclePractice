# Oracle Practice 07/07/2022

## Rearrange Products Table

- SQL schema:

  ![find_total_time_spent_by_each_employee_sql_schema](../img_sql_schema/7/7_find_total_time_spent_by_each_employee_sql_schema.png)

- Example:

  ![find_total_time_spent_by_each_employee](../img_example/7/7_find_total_time_spent_by_each_employee.png)

- <ins>query:</ins>

  ```sql
  select
    to_char(event_day,'yyyy-mm-dd') as day,
    emp_id,
    sum(out_time - in_time) as total_time
  from Employees
  group by event_day, emp_id
  ```
