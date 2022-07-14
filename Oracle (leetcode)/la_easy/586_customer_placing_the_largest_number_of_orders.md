# Oracle Practice 08/07/2022

## Customer Placing the Largest Number of Orders

- SQL schema:

  ![customer_placing_the_largest_number_of_orders_sql_schema](../img_sql_schema/7/8_customer_placing_the_largest_number_of_orders_sql_schema.png)

- Example:

  ![customer_placing_the_largest_number_of_orders](../img_example/7/8_customer_placing_the_largest_number_of_orders.png)

- <ins>query:</ins>

  ```sql
  select *
  from
  (
    select customer_number
    from Orders
    group by customer_number
    order by count(customer_number) desc
  )
  where rownum=1;
  ```
