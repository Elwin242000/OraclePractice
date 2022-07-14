# Oracle Practice 05/07/2022

## Tree Node

- SQL schema:

  ![tree_node_sql_schema](../img_sql_schema/7/5_tree_node_sql_schema.png)

- Example:

  ![tree_node_1](../img_example/7/5_tree_node_1.png)
  ![tree_node_2](../img_example/7/5_tree_node_2.png)

- <ins>query:</ins>

  ```sql
  select
    id,
    case
        when p_id is null then 'Root'
        when id in (
            select distinct p_id
            from Tree
        ) then 'Inner'
        else 'Leaf'
    end as type
  from Tree
  ```
