# Oracle Practice 23/06/2022

## Patients With A Condition

- SQL schema:

  ![patients_with_a_condition_sql_schema](../img_sql_schema/7/5_patients_with_a_condition_sql_schema.png)

- Example:

  ![patients_with_a_condition](../img_example/7/5_patients_with_a_condition.png)

- <ins>query:</ins>
  ```sql
  select
    patient_id,
    patient_name,
    conditions
  from Patients
  where conditions like 'DIAB1%'
    or conditions like '% DIAB1%'
  ```
