# Oracle Practice 07/07/2022

## Customer Who Visited but Did Not Make Any Transactions

- SQL schema:

  ![customer_who_visited_but_did_not_make_any_transactions_sql_schema](../img_sql_schema/7/7_customer_who_visited_but_did_not_make_any_transactions_sql_schema.png)

- Example:

  ![customer_who_visited_but_did_not_make_any_transactions](../img_example/7/7_customer_who_visited_but_did_not_make_any_transactions.png)

- <ins>query:</ins>
  ```sql
  select
    customer_id,
    count(*) count_no_trans
  from
  (
    select
      customer_id,
      visit_id
    from Visits
    where visit_id not in (
        select distinct visit_id
        from Transactions
    )
  )
  group by customer_id
  order by customer_id
  ```
