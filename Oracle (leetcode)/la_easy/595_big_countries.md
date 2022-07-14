# Oracle Practice 06/07/2022

## Big Countries

- SQL schema:

  ![big_countries_sql_schema](../img_sql_schema/7/6_big_countries_sql_schema.png)

- Example:

  ![big_countries](../img_example/7/6_big_countries.png)

- <ins>query:</ins>
  ```sql
  select
    name,
    population,
    area
  from World
  where area >= 3000000
    or population >= 25000000
  ```
