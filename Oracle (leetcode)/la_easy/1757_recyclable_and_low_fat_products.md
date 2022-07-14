# Oracle Practice 06/07/2022

## Recyclable and Low Fat Products

- SQL schema:

  ![recyclable_and_low_fat_products_sql_schema](../img_sql_schema/7/6_recyclable_and_low_fat_products_sql_schema.png)

- Example:

  ![recyclable_and_low_fat_products](../img_example/7/6_recyclable_and_low_fat_products.png)

- <ins>query:</ins>
  ```sql
  select product_id
  from Products
  where low_fats = 'Y'
    and recyclable = 'Y'
  ```
