 ### 📖 ***Eclat Algorithm***

The Eclat algorithm (Equivalence Class Clustering and bottom-up Lattice Traversal) is a popular algorithm for frequent itemset mining and association rule learning over transactional databases. It is particularly useful in market basket analysis to discover interesting relationships between items purchased together.


### 💡 ***The algorithm follows these steps:***

Vertical Data Representation:

Convert the horizontal transactional database into a vertical database. Each item is represented with a Transaction ID (TID) list, which includes all transactions where the item appears.Recursive Depth-First Search: Recursively generate the itemsets and their corresponding TID sets by intersecting the TID lists of items.

Generate Candidate Itemsets:

Combine items by intersecting their TID lists. The intersection of TID lists represents transactions where both items appear together.

Filter by Minimum Support Threshold:

Retain only those itemsets whose support (number of transactions in the TID list) meets or exceeds the minimum support threshold.

Once you have identified the frequent itemsets using the Eclat algorithm, the next task is to generate association rules :

Generate Subsets:

Create all non-empty subsets of each frequent itemset.

Create Association Rules:

For each subset 𝑋, generate rules of the form 𝑋→𝑌 , where Y is the remaining items in the itemset.

Calculate Confidence:

Calculate the confidence for each rule X→Y.

Apply Minimum Confidence: 

Filter out rules with confidence below the minimum threshold.
 Calculate Lift: 
 
 calculate the lift to evaluate the strength of the rule.
 
Output :

All rules with there lift and Confidence.


### ✅ ***Advantages***

Simplicity: The algorithm is relatively simple to implement and understand.
Memory Usage: Eclat can handle large datasets efficiently by using vertical data representation.


### 🔍***Use Cases***

Market Basket Analysis: Discovering frequent itemsets in retail transactions to understand customer purchasing behavior.
Web Usage Mining: Analyzing web logs to find frequently accessed pages together.
Bioinformatics: Identifying frequent patterns in gene sequences.
