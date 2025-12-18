Fairness will need customer segmentation. It is a measure of how *fair* the rec system is across different groups.
Trivial example of groups are man vs woman



Fairness across users [[user_fairness]]
- To calculate, need
  - Avg predicted score for the jth item from dis + advantage users
  - Avg ratings for dis + advantage user
> What are ratings?
In our example, we must decide on what the rating system is.
Should we take watchlist, bid, and wins into consideration?
Example breakdowns
Binary - click item = 1, didn't click item = 0
Weighted - click item = 1, watchlist = 3, bid/buy = 5
View no click - click item = 1, viewed item .1 or other

Fairness across items [[item_fairness]]



[user_fairness]: user_fairness.md "user_fairness"
[item_fairness]: item_fairness.md "item_fairness"
