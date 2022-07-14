# Oracle Practice 30/06/2022

## Game Play Analysis I

- SQL schema:

  ![game_play_analysis_1_sql_schema](../img_sql_schema/6/30_game_play_analysis_1_sql_schema.png)

- Example:

  ![game_play_analysis_1](../img_example/6/30_game_play_analysis_1.png)

- <ins>query:</ins>
  ```sql
  select
    player_id,
    to_char(min(event_date),'yyyy-mm-dd') as first_login
  from Activity
  group by player_id
  ```
