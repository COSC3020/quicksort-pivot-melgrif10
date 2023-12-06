[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12562103&assignment_repo_type=AssignmentRepo)
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

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions. 

The median of three method selects an element from the begining, middle, and end of the array and selects the median value of those three as the pivot. Choosing the leftmost element of the array just selects the first element as the pivot. In order to pick a good pivot we want the value to be in the middle n/2 of elements. A good pivot will create two partitions with a maximum size of 3n/4 and has $\varTheta (nlog(n))$ comparisons. Ensuring that the partitions are realativley balanced makes it less likely for the algorithm to run into the worst-case scenario. Now that a good pivot has been defined analysis on the median of three vs the first element of selecting a pivot can begin. 

 The median of three chooses elements from the begining, middle, and end of the array and chooses the median of the three as a pivot. This method has a larger sample size for choosing a pivot which gives you more of a chance of choosing a good pivot. The elements at the begining and middle of the array might not have a value that lies in the middle n/2 of the array but the end value could. And when you compare the multiple values from the array with one another and choose the median it increases your chances of getting a value that creates partitons with a max size of 3n/4. When you just choose the first element there is less of a probability of choosing a good pivot because you get stuck with whatever value that may be. 
