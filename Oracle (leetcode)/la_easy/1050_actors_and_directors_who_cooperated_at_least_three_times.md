# Oracle Practice 08/07/2022

## Actors and Directors Who Cooperated At Least Three Times

- SQL schema:

  ![actors_and_directors_who_cooperated_at_least_three_times_sql_schema](../img_sql_schema/7/8_actors_and_directors_who_cooperated_at_least_three_times_sql_schema.png)

- Example:

  ![actors_and_directors_who_cooperated_at_least_three_times](../img_example/7/8_actors_and_directors_who_cooperated_at_least_three_times.png)

- <ins>query:</ins>

  ```sql
  select
    actor_id,
    director_id
  from ActorDirector
  group by actor_id, director_id
  having count(*) >= 3
  ```
