# Oracle Practice 23/06/2022

## Second Highest Salary

- SQL schema:

  ![second_highest_salary_sql_schema](../img_sql_schema/6/23_second_highest_salary_sql_schema.png)

- Example:

  ![second_highest_salary](../img_example/6/23_second_highest_salary.png)

- <ins>query:</ins>
  ```sql
  select
    max(salary) as "SecondHighestSalary"
  from Employee
  where salary not in (
    select
      max(salary)
    from Employee
  )
  ```
