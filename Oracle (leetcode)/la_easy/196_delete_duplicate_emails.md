# Oracle Practice 30/06/2022

## Delete Duplicate Emails

- SQL schema:

  ![delete_duplicate_email_sql_schema](../img_sql_schema/6/30_delete_duplicate_email_sql_schema.png)

- Example:

  ![delete_duplicate_email](../img_example/6/30_delete_duplicate_email.png)

- <ins>query:</ins>
  ```sql
  delete from Person
  where id in
  (
    select a.id
    from
    (
        select
          id,
          row_number() over (partition by email order by id) rn
        from Person
    ) a
    where a.rn > 1
  )
  ```
