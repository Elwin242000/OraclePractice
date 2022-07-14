# Oracle Practice 23/06/2022

## Swap Salary

- SQL schema:

  ![swap_salary_sql_schema](../img_sql_schema/7/4_swap_salary_sql_schema.png)

- Example:

  ![swap_salary](../img_example/7/4_swap_salary.png)

- <ins>query:</ins>
  ```sql
  update Salary
  set sex = case
    when sex = 'm' then 'f'
    else 'm'
  end
  ```
