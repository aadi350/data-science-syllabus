# Coding
1. Calculate the share of new and existing users. Output the month, share of new users, and share of existing users as a ratio. New users are defined as users who started using services in the current month. Existing users are users who started using services in the current month and used services in any previous month. Assume that the dates are all from the year 2020

| id | time_id | user_id | customer_id | client_id | event_types | event_id |
| --- | --- | --- | --- | --- | --- | --- |
|1|2020-02-28| 3434-AQEFN | Sendif | desktop | message_sent | 3

```SQL 
with all_users as (
    SELECT date_part('month', time_id) AS month,
           count(DISTINCT user_id) as all_users
    FROM fact_events
    GROUP BY month),
new_users as (
    SELECT date_part('month', new_user_start_date) AS month,
           count(DISTINCT user_id) as new_users
    FROM
         (SELECT user_id,
           min(time_id) as new_user_start_date
          FROM fact_events
          GROUP BY user_id) sq
    GROUP BY month
)
SELECT
  au.month,
  new_users / all_users::decimal as share_new_users,
  1- (new_users / all_users::decimal) as share_existing_users
FROM all_users au
JOIN new_users nu ON nu.month = au.month

```