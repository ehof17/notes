#### Fairness across items
https://dl.acm.org/doi/epdf/10.1145/3292500.3330745
*Pairwise fairness*

*Pairwise Accuracy*
- What is the probability that a clicked item is ranked above anoher relevant unclicked item, for the same query?

*Pairwise fairness*
- Likelihood of a clicked item being ranked above another relevant unclicked item is the same across both groups, conditioned on the items have been engaged with the same amount
- Doesn't distinguish types of misorderings
- [A2, A3, B1, A1, B2, B3] A1 clicked
- [A1, A2, A3, B1, B2, B3] B1 clicked
- Pairwise accuracy is 2/5
- Both are bad since the clicked item was ranked low
- Second case, even when an item from group B was clicked, all group B items are ranked below

*Intra group pairwise fairness*
- If likelihood of a clicked item being ranked above another relavent unclicked item from the same group is the same independent of group, conditioned on the itmes have been engaged with the same amount

*Inter-Group pairwise fairness*
- Opposite group
  