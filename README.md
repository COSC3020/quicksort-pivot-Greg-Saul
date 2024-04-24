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

### Explanation

as shown in the slides, there is a 1/2 chance of getting a good pivot and a 1/2 chance of getting high or low(1/4 each)

if we use this information to make a table of all of the possible permutations, then add up the individual chances of getting a good pivot, we should have a numerical representation of the likelyhood of getting a good pivot each time we choose one

|case|probability|
|:-------------|:-------------|
|good pivot|$\frac{1}{2}$|
|bad(low)|$\frac{1}{4}$|
|bad(high)|$\frac{1}{4}$|

now lets consider the cases for the median of three using hi, g, lo. I will only include the cases that have a good pivot for this chart
|case|probability|how many good|
|:-------------|:-------------|:---------------
|g,g,g|$\frac{1}{2} * \frac{1}{2} * \frac{1}{2}$|3|
|lo,g,g|$\frac{1}{4} * \frac{1}{2} * \frac{1}{2}$|2|
|g,lo,g|$\frac{1}{2} * \frac{1}{4} * \frac{1}{2}$|2|
|g,g,lo|$\frac{1}{2} * \frac{1}{2} * \frac{1}{4}$|2|
|hi,g,g|$\frac{1}{4} * \frac{1}{2} * \frac{1}{2}$|2|
|g,hi,g|$\frac{1}{2} * \frac{1}{4} * \frac{1}{2}$|2|
|g,g,hi|$\frac{1}{2} * \frac{1}{2} * \frac{1}{4}$|2|
|lo,lo,g|$\frac{1}{4} * \frac{1}{4} * \frac{1}{2}$|1|
|lo,g,lo|$\frac{1}{4} * \frac{1}{2} * \frac{1}{4}$|1|
|g,lo,lo|$\frac{1}{2} * \frac{1}{4} * \frac{1}{4}$|1|
|hi,hi,g|$\frac{1}{4} * \frac{1}{4} * \frac{1}{2}$|1|
|hi,g,hi|$\frac{1}{4} * \frac{1}{2} * \frac{1}{4}$|1|
|g,hi,hi|$\frac{1}{2} * \frac{1}{4} * \frac{1}{4}$|1|

if we combine these cases we get -> $6(\frac{1}{2} * \frac{1}{4} * \frac{1}{4}) + 6(\frac{1}{2} * \frac{1}{2} * \frac{1}{4}) + (\frac{1}{2} * \frac{1}{2} * \frac{1}{2})$

this gives us $0.125+0.375+0.1875$

if we add these up and multiply by 100 to get a percentage we get $68.75$% likelyhood of choosing a good pivot that is in the middle of the dataset

this shows that we are more likely to get a good pivot because with the leftmost pivot method we get a good pivot only about $\frac{1}{2}$ of the time but with the median of three method, we should get a good pivot <strong><em>about</em></strong> $\frac{2}{3}$ of the time.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.





### source

https://www.youtube.com/watch?v=_DI3-pHg-1Q -> helped me get a better visual understanding of pivot selection methods.

asked tyler laceby for help and he explained the basics of how to set up the problem... and reminded me what permutation means




