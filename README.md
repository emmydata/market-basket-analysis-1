# Cross Selling

What is cross selling? Cross selling is the ability to sell more products to a customer by analyzing the customer’s shopping trends as well as general shopping trends and patterns which are in common with the customer’s shopping patterns.

Market Basket Analysis with Association Rule-Mining
The whole concept of association rule-mining is based on the concept that customer purchase behavior has a pattern which can be exploited for selling more items to the customer in the future.

we can use these rules to develop bundles of products which make it convenient for the customer to buy these items together. Another way to use these rules is to bundle products along with some discounts for other relevant products in the bundle, hence ensuring that the customer becomes more likely to buy more items.

There are some vital concepts pertaining to association rule-mining and they are:

1. Itemset: Itemset is just a collection of one or more items that occur together in a transaction. For example, here {milk, bread} is example of an itemset.

2. Support: Support is defined as number of times an itemset appears in the dataset. Mathematically it is defined as:

supp ( { beer , diaper } ) = number of transactions with beer and diaper / total transactions

3. Confidence: Confidence is a measure of the times the number of times a rule is found to exist in the dataset. For a rule which states { beer ® diaper } the confidence is mathematically definedas:
   confidence ( { beer , diaper } ) = supp ( beer and diaper ) supp ( beer )

4. Lift: Lift of the rule is defined as the ratio of observed support to the support expected in the case the elements of the rule were independent. For the previous set of transactions if the rule is defined as { X ® Y } , then the lift of the rule is defined as:
   lift ( X ® Y ) = supp ( X U Y )/ ( supp ( X ) \* supp ( Y ) )

5. Frequent itemset: Frequent itemsets are itemsets whose support is greater than a user defined support threshold.

## FP Growth Algorithm

Take in the transactional database and create an FP-tree structure to represent frequent itemsets.

Divide this compressed representation into multiple conditional datasets such that each one is associated with a frequent pattern.

Mine for patterns in each such dataset so that shorter patterns can be recursively concatenated to longer patterns, hence making it more efficient.
