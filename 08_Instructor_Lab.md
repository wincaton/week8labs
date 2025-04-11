# Instructor-led Lab: Advanced Data Manipulation

In this assignment you will practice your new skills in data manipulation with the *piping* expression for `pandas`. Please follow the instructions below.

## Sorting and Ordering Data

Last week you sorted, ordered, and filtered the data [github_teams.csv](/data/github_teams.csv) using basic pandas techniques. Now that you have learned to use advanced techniques relying on piping expressions, you will perform the similar operations again, but with your new skills. 

Please perform the following operations in order:

* Select the columns `Team_type`, `human_work`, and `work_per_human`.
* Select columns that end in the letter `t`. Use the regex `t$`.
* Sort your data descending using the columns `Team_size_class`, `human_work`, `work_per_human`.
* Select `human-bot` teams that have a `bot_members_count` value greater than and equal to 3.
* Find the `human` teams that are `Large` and have a `human_gini` value greater than and equal to 0.75.
* How many teams are in the `Small` or `Large` category?
* How many teams are in the `Small` or `Large` category with a `human_gini` value less than and equal to 0.25?
* How many `human` teams are in the `Medium` category?
* Save the columns `Team_size_class` and `work_per_human` as a new DataFrame.
* Rename these two columns in the new DataFrame. Change `human_gini` to `work_inequality` and `eval_survival_day_median` to `issue_resolution_time`.
