# Oracle Practice 27/06/2022

## Duplicate Emails

- SQL schema:

  ![duplicate_emails_sql_schema](../img_sql_schema/6/27_duplicate_emails_sql_schema.png)

- Example:

  ![duplicate_emails](../img_example/6/27_duplicate_emails.png)

- <ins>query:</ins>
  ```sql
  select
    email as "Email"
  from Person
  group by email
  having count(email) > 1
  ```
