# divar-data-analyst-summercamp-task
This repository contains the entrance task submission for Divar's Data Analyst summer camp. The detailed version of the explanation is found in `task.pdf`, which is written in Persian.

## Dataset Explanation
Each user in the Divar application can search a query and receive some results. Then he/she can click on any of the shown results. Results are sorted by Time (and not relevance). This dataset contains the behavior of some users during a specific day. Each row of this dataset is equivalent to an action taken by a user. The columns are explained below:
- **action:** The user action, either loading a page (`load_post_page`) or clicking on a post (`click_post`).
- **created_at:** The timestamp of an action.
- **source_event_id:** Unique id for each query.
- **device_id:** Unique id for each user.
- **post_page_offset:** The loaded page index. Exclusive to `load_post_page` action.
- **tokens:** The unique ids of the posts loaded on a page. Exclusive to `load_post_page` action.
- **post_index_in_post_list:** Rank of a clicked post. Exclusive to `click_post` action.
- **post_token:** Unique id of a clicked post. Exclusive to `click_post` action.

## Question 1
Find a few flaws in the dataset (5 at max). A table or plot could be provided for each flaw/error.

## Question 2
Calculate these metrics:
- **Dark Query Percentage:** Percentage of queries for which <10 results were shown.
- **Query Bounce Rate:** Percentage of queries for which none of the shown results were clicked on.

## Question 3
In order to estimate user satisfaction, four metrics are introduced below **for each query**. Which one do you think is the best and why? Explain in one or two paragraphs. Calculate the mean of chosen metric for all of the queries.
1. Percentage of clicked posts to loaded posts.
2. Rank of the first clicked post.
3. Average rank of all the clicked posts.
4. Is any of the first three shown results clicked on?

## Question 4
The introduced metrics in the previous question are closely related. To understand the relationship, review the Bernoulli distribution. Using this distribution, can we make a simple model to predict the user's click behavior? Using this model, if we had any of those four metrics, could we calculate an estimate for the other 3? (explain in one page)

`submission.pdf` contains the EDA and answers written in Persian and `submission.ipynb` contains the Python code of each section.
