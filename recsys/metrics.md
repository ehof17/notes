### Different evaluation properties
Business-oriented
- Click-through rate (CTR)
- Adoption and conversion rate
- Sales and revenue

Prediction accuracy
- Mean absolute error (MAE)
- (Root) Mean squared error ((R)MSE)

Usage prediction
- Recall, precision, F-score
- Receiver operating characteristic curve (ROC)
- Area under ROC curve (AUC)

Ranking
- Normalized discounted cumulative gain (NDCG)
- Mean reciprocal rank (MRR)

Novelty
- Item novelty
- Global long-tail novelty

Diversity
- intra-list similarity (ILS)

Coverage
- Item coverage
- User space coverage
- Gini index

Serendipity [[serendipity]]
- Unexpectedness
- Serendipity

Fairness across users [[user_fairness]]
- Value unfairness
- Absolute unfairness
- Over/underestimation of fairness

Fairness across items [[item_fairness]]
- Pairwise fairness
- Disparate treatment ratio (DTR)	
- Equal expected exposure	
- Equity of amortized attention
- Disparate impact ratio (DIR)	
- Viable A test






##### What's needed
- Customer segmentation
  - Trivial example of man v woman or more distinct properties
- Among these groups after splitting up, gather fairness metrics


- Each of the metrics have a straight forward subgradient and can be optimized by various means 


###### Rating 
- binary 1 click 0 no click
- 
###### Weighted implicit rating
- view = 0.1, click = 1, watchlist = 2, purchase = 5
###### Exposeure aware 
- if given impression but not clicked

- Need to track stuff

- Randomized experiments over a small percentage of queries
- 
  - Pair of items in positions 2 or 3 of the reccomended slate
  - 2 items are selected at random, and their order is Randomized
  - Among all queries in the experimental slice only a small fraction will have clicks on one of the items in the randomized pairity
  - When an item in the randomized pair is clicked
    - Record query, pair, which item clicked, and subsequent engagement z


##### How to improve said metrics
###### Pairwise fairness:
- Optimize for equality of opportunity in classification
  - Minimize the correlation between group membership and the model's prediction among examples with the same label.
  ![Objective function](recsys/loss_objective.png)

- P is the pairs of tuples (Query, Pair, Clicked, Engagement)
- ((q,j,y,z), (q, j', y', z'))

- 


[item_fairness]: item_fairness.md "item_fairness"
[user_fairness]: user_fairness.md "user_fairness"





[serendipity]: serendipity.md "serendipity"
