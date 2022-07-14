# Oracle Practice 08/07/2022

## Top Travellers

- SQL schema:

  ![top_travellers_sql_schema](../img_sql_schema/7/8_top_travellers_sql_schema.png)

- Example:

  ![top_travellers](../img_example/7/8_top_travellers.png)

- <ins>query:</ins>
  ```sql
  select
    a.name,
    nvl(sum(b.distance),0) as travelled_distance
  from Users a left join Rides b on a.id = b.user_id
  group by a.name
  order by travelled_distance desc, a.name asc
  ```
