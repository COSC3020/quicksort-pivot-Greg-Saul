[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/IF3rQO50)
# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

###Explanation

The median of three is the better option when compared to just choosing the left most number. This is because if we take the middle number in a set of three, it guarantees that we will not have the worst case in which either the biggest or smallest number is chosen.

Numerical explanation

we can represent this numerically by comparing the probabilities that we get a better pivot. In the left pivot choice we have a $1$ in $n$ chance of picking the best pivot but in the median of three method, there is a $3$ in $n$ chance because we look at three numbers and choose the best instead of only looking at one number. We can simply compare the numbers $\frac{1}{n}<\\frac{3}{n}$ this clearly states that the likelyhood of getting a good pivot is 3 times higher with the median of three method.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.





###source

https://www.youtube.com/watch?v=_DI3-pHg-1Q -> helped me get a better visual understanding of pivot selection methods.




