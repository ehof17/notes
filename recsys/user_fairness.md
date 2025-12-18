#### Fairness Across users
https://proceedings.neurips.cc/paper_files/paper/2017/file/e6384711491713d29bc63fc5eeb5ba4f-Paper.pdf
Population imbalance and observational bias can lead to unfair system
*Population Bias*
- Different users in the same dataset with varied frequencies
- Men and women in stem. More men than women

*Observational Bias*
- Never reccomended item, never see item, alg never learns. So a man that doesn't like stem might get items that aren't tailored to his specific liking and there is no way to fix it

*Value Unfairness* 
- Inconsistency in signed estimation error across the user types
- Occurs when one class of user is given higher or lower preds than true pref. 
- If a man doesn't like stem they might be reccomended stem topics just since they are man
![Value Unfairness](valueUnfairness.png)
- To calculate, need
  - Avg predicted score for the jth item from dis + advantage users
  - Avg ratings for dis + advantage user

*Absolute Unfairness*
- Inconsistency in absolute estimation error across user types
- If one user type has small reconstruction error and the other user type has large reconstruction error, one user has good rec and another has bad rec
- If female given .5 + and male given -.5, then no abs unfairness.
- If female +2 and male +1, abs is high and value unfairness may be lower

*Underestimation unfairness*
- Inconsistency in how much the predictions underestimate true ratings
- Important where missing recs are more critical than extra recs
  - Top student not being recommended thing they will excel in
  - Customer not buying a trailer they would be interested in

*Overestimation unfairness*
- Predictions overestimating true ratings
- Important in settings where users mau be overwhelmed, too many recs would be detremental
- If users must invest large amounts of time to evaluate each recommended item
  - Could be for businesses

*Non pairity unfairness*
- Absolute difference between the overall average ratings of disadvantaged users and those of advantaged users


- Imagine if it is a corporation on AT buying a lot of items, underestimation unfairness is critical
- If its a mom and pop shop buying a machine for the first time, overestimation unfairness is more critical
