# Oracle Practice 08/07/2022

## Sales Person

- SQL schema:

  ![sales_person_1_sql_schema](../img_sql_schema/7/8_sales_person_sql_schema_1.png)
  ![sales_person_2_sql_schema](../img_sql_schema/7/8_sales_person_sql_schema_2.png)

- Example:

  ![sales_person](../img_example/7/8_sales_person.png)

- <ins>query:</ins>

  ```sql
  select distinct name
  from SalesPerson
  where sales_id not in (
    select o.sales_id
    from Orders o inner join Company c on o.com_id = c.com_id
    where c.name = 'RED'
  )
  order by name
  ```
