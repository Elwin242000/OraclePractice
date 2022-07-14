# Oracle Practice 24/06/2022

## Rank Scores

- SQL schema:

  ![rank_scores_sql_schema](../img_sql_schema/6/24_rank_scores_sql_schema.png)

- Example:

  ![rank_scores](../img_example/6/24_rank_scores.png)

- <ins>query:</ins>
  ```sql
  select
    score "score",
    dense_rank() over (order by score desc) "rank"
  from Scores
  ```
