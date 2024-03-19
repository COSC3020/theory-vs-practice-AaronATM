[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

1:

- Actual performance of programs/algorithms can also rely heavily on the hardware being used to run them. With how performative computers are in this day, you might not even notice a difference, depending on the input size and the optimization.
  
- The difference in performance that we are sometimes talking about with asymptotic analysis can to be very minuscule between different algorithms. With this in mind, there are many cases where the difference in performance can be functionally the same, within margin of error, rounding based on significant figures of runtime calculation, etc.
  
- Opposite of the other two reasons, depending on the notation used (big/little o, $\theta$, etc) the difference in functions can stray far. In this case, the difference in runtime with a small input size can actually be larger while the difference in runtime with a large input size can be smaller.

2:

log(1000) = 3 seconds
actual time: 5 seconds

log(10000) * 5/3 = 6.67 seconds

Reasoning: Using the average case runtime complexity for a binary search tree (O(logn)) we can guess that a tree with 1000 elements would have a find function that takes around 3 seconds, however the actual time is 5 seconds. If we create a ratio of actual time to theoretical time, we can guess that the actual runtime based on input would 5/3 of the runtime calculated through asymptotic analysis. Thus, for an input of 10,000 elements I would guess that it should take an average of 6.67 seconds to find a particular element.
 
3:

- I used the average case asymptotic complexity in order to perform the calculations in the previous question, which is not always how the time complexity will work out depending on how the elements are put into the tree in the first place.

- The specific element that we are looking for could be very deep into the tree, which would have a large effect on how long it takes to actually find

- The implementation of the binary search tree in code could be suboptimal, especially depending on the language and how comparisons are called. In this case, the asymptotic complexity only focuses on the actual algorithm in regards to input size, and not the physical implementation of the data structure.
