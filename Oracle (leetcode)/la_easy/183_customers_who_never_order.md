# Oracle Practice 28/06/2022

## Customers Who Never Order

- SQL schema:

  ![customer_who_never_order_sql_schema](../img_sql_schema/6/28_customer_who_never_order_sql_schema.png)

- Example:

  ![customer_who_never_order](../img_example/6/28_customer_who_never_order.png)

- <ins>query:</ins>
  ```sql
  select
    name as "Customers"
  from Customers
  where id not in (
    select
      customerId
    from Orders
  )
  order by name
  ```
