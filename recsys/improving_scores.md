##### Improving seredipity [[serendipity]]
Re-Rank results to increase diversity while maintaining relevance
- Maximal Marginal relevance
- Linear combo of items relavence and negative of maximum similarity to items already in the result list


##### Improving item fairness [[item_fairness]]
Pairwise fairness:
- Optimize for equality of opportunity in classification
  - Minimize the correlation between group membership and the model's prediction among examples with the same label.
  ![Objective function](recsys/loss_objective.png)

- P is the pairs of tuples (Query, Pair, Clicked, Engagement)
- ((q,j,y,z), (q, j', y', z'))

- 


###### Improving reward signals
1. Decide on what reward we are looking for
- Clicks/Revenue
2. Split on population, find the difference of the value that they provide



[item_fairness]: item_fairness.md "item_fairness"


[serendipity]: serendipity.md "serendipity"
