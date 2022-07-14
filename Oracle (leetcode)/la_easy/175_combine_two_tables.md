# Oracle Practice 23/06/2022

## Combine Two Tables

- SQL schema:

  ![combine_2_table_sql_schema](../img_sql_schema/6/23_combine_2_table_sql_schema.png)

- Example:

  ![combine_2_table](../img_example/6/23_combine_2_table.png)

- <ins>query:</ins>
  ```sql
  select
    p.firstName,
    p.lastName,
    a.city,
    a.state
  from Person p
    left join Address a on p.personId = a.personId
  ```
