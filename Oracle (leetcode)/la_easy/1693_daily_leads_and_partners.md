# Oracle Practice 07/07/2022

## Daily Leads and Partners

- SQL schema:

  ![daily_leads_and_partners_sql_schema](../img_sql_schema/7/7_daily_leads_and_partners_sql_schema.png)

- Example:

  ![daily_leads_and_partners](../img_example/7/7_daily_leads_and_partners.png)

- <ins>query:</ins>
  ```sql
  select
    to_char(date_id,'yyyy-mm-dd') as date_id,
    make_name,
    count(distinct lead_id) as unique_leads,
    count(distinct partner_id) as unique_partners
  from DailySales
  group by date_id, make_name
  ```
