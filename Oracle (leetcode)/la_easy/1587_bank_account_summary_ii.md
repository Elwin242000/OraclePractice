# Oracle Practice 07/07/2022

## Bank Account Summary II

- SQL schema:

  ![bank_account_summary_ii_sql_schema](../img_sql_schema/7/7_bank_account_summary_ii_sql_schema.png)

- Example:

  ![bank_account_summary_ii](../img_example/7/7_bank_account_summary_ii.png)

- <ins>query:</ins>
  ```sql
  select
    a.name,
    sum(b.amount) balance
  from Users a inner join Transactions b on a.account = b.account
  group by a.account, a.name
  having sum(b.amount) > 10000
  ```
