# Independent Lab: Advanced Data Manipulation

In this assignment, you will use advanced functions in `pandas` to query and filter data. These functions reduce workload by simplifying and reducing code.

Please use the [gh_turnover_four_projects.csv](data/gh_turnover_four_projects.csv) file provided in the data folder to complete the tasks outline below. 

*Data Summary*: This dataset contains information about four projects hosted on GitHub and the contributors to those projects over a period of time. The dataset represents a subset of data that has been combined and aggregated from the data published by Vasilescu et al. in [their 2015 Mining Software Repositories conference paper](http://doi.org/10.1109/MSR.2015.77). The data in gh_turnover_four_projects.csv were prepared by me (Olivia B. Newton) for an analysis of turnover in GitHub projects. To make the dataset more manageable for the assignment, I have selected four projects from my original dataset which includes data for over 22,000 projects.

## Rename Columns

Import the file `gh_turnover_four_projects.csv`. Once imported, rename columns like so:

* `domain` change to `project_domain`
* `language` change to `project_language`
* `windows` change to `project_age`
* `window_idx` change to `quarter`
* `num_team` change to `team_size`
* `num_commits` change to `project_commits`
* `blau_gender` change to `gender_blau`
* `Gini_gh_ten` change to `gh_tenure_gini`
* `Core1` change to `core_dev`
* `commits` change to `user_commits`
* `propCommits` change to `commit_proportion`
* `github_tenure` change to `gh_tenure`
* `leavesNextQ` change to `leaves_next_q`
* Leave all other column names as is

## Data Wrangling

It is time to practice your data wrangling skills with Python! Please perform the following tasks. **Run all code in your notebook, then save your notebook with output**.

Note, some of the tasks ask you to use regular expressions. We have not covered this in class, so I have provided the regex syntax. If parentheses are included as part of the regex, include it. For example, I provide `(^p)` below. Thus, your code would be `.filter(regex = '(^p)')`.

1. Calculate the mean of `user_commits`. 
2. Calculate the median of `user_commits`.
3. Select all columns that start with a *p* (i.e., `(^p)`) **or** contain an *g* (i.e., `(g)`). Save it as a new DataFrame named `turnover_new`. Output the columns in your notebook.
4. Using your newly created DataFrame `turnover_new`, select rows in which `project_commits` is greater than 9,000.
5. Using pandas piping notation, perform the previous two operations together and save it as a new DataFrame `turnover_newer`. This means you should select columns that start with a *p* or contain an *g* and select rows in which `project_commits` is greater than 9,000.

For the following tasks, *do not use* `turnover_new` or `turnover_newer`. Instead, use the original DataFrame you initially created from the provided file.

1. Using pandas piping notation, select all columns that end with the letter *e* (i.e., `e$`) or contain the letter *s* (i.e., `s`). Additionally, select rows in which `gh_tenure` is greater than or equal to 1,991. 
2. Use the query you just performed. You will calculate the mean and median of `user_commits`. How does it compare to the answers above in which you calculated the mean and median? Please provide your answer in a Markdown cell within your notebook.
