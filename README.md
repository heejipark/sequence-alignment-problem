# Sequence-Alignment-Problem
CSCI570 (Analysis of Algorithms) Project - Implement the basic Dynamic Programming solution to the Sequence Alignment problem.


### Algorithm Description

Suppose we are given two strings π and π, where π consists of the sequence of symbols π₯ and consists of the sequence of symbols . π₯1, π₯2 , ... , π₯π π π¦1, π¦2 , ... , π¦π. Consider the sets {1, 2, ... ,π} and {1, 2, ... , π} as representing the different positions in the strings π and π, and consider a matching of these sets; Recall that a matching is a set of ordered pairs with the property that each item occurs in at most one pair. We say that a matching π of these two sets is an alignment if there are no βcrossingβ pairs: if (π, π), (π', π') Ο΅ π and π < π' , then π < π'. Intuitively, an alignment gives a way of lining up the two strings, by telling us which pairs of positions will be lined up with one another.
<br>
Our definition of similarity will be based on finding the optimal alignment between π and π, according to the following criteria. Suppose π is a given alignment between π and π:
1. First, there is a parameter Ξ΄ that defines a gap penalty. For each π > 0 position of πor π that is not matched in π β it is a gap β we incur a cost of Ξ΄.
2. Second, for each pair of letters π, π in our alphabet, there is a mismatch cost of Ξ± for lining up with . Thus, for each , we pay the π π (π,π) Ο΅ π appropriate mismatch cost Ξ± for lining up with . One generally π₯π π¦π assumes that Ξ± = 0 for each letter βthere is no mismatch cost to line up π a letter with another copy of itselfβalthough this will not be necessary in anything that follows.
3. The cost of π is the sum of its gap and mismatch costs, and we seek an alignment of minimum cost.