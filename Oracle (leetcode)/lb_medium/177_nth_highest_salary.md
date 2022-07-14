# Oracle Practice 23/06/2022

## Nth Highest Salary

- SQL schema:

  ![nth_highest_salary_sql_schema](../img_sql_schema/6/23_nth_highest_salary_sql_schema.png)

- Example:

  ![nth_highest_salary](../img_example/6/23_nth_highest_salary.png)

- <ins>query:</ins>

  ```sql
  CREATE FUNCTION getNthHighestSalary(N IN NUMBER) RETURN NUMBER IS
  result NUMBER;
  BEGIN
        SELECT DISTINCT SALARY
        INTO RESULT
        FROM (
            SELECT
              E.ID,
              E.SALARY,
              DENSE_RANK() OVER ( ORDER BY SALARY DESC) RANK
            FROM Employee E
        )
        WHERE RANK=N;
    RETURN result;
  END;
  ```
