# Oracle Practice 08/07/2022

## Classes More Than 5 Students

- SQL schema:

  ![classes_more_than_5_students_sql_schema](../img_sql_schema/7/8_classes_more_than_5_students_sql_schema.png)

- Example:

  ![classes_more_than_5_students](../img_example/7/8_classes_more_than_5_students.png)

- <ins>query:</ins>

  ```sql
  select class
  from Courses
  group by class
  having count(*) >= 5
  ```
