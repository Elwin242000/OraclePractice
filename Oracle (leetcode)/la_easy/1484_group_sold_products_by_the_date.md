# Oracle Practice 23/06/2022

## Group Sold Products By The Date

- SQL schema:

  ![group_sold_products_by_the_date_sql_schema](../img_sql_schema/7/5_patients_with_a_condition_sql_schema.png)

- Example:

  ![group_sold_products_by_the_date](../img_example/7/5_patients_with_a_condition.png)

- <ins>query:</ins>
  ```sql
  select
    to_char(sell_date,'yyyy-mm-dd') sell_date,
    count(*) num_sold,
    listagg (product,',') within group (order by product) products
  from
  (
    select distinct *
    from Activities
  ) a
  group by sell_date
  ```
