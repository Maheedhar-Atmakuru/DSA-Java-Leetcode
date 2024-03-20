```
class Solution {
    public int maxSubArray(int[] nums) {
        int maxSoFar = nums[0];
        int currentSum = nums[0];
        
        for(int i = 1; i < nums.length; i++) {
            if (currentSum < 0) {
                currentSum = 0;
            }
            currentSum = currentSum + nums[i];
            if (currentSum > maxSoFar) {
                maxSoFar = currentSum;
            }
        }
        
        return maxSoFar;
    }
}
```

### Introduction:
Algorithms play a vital role in computer science, helping to solve complex problems in a structured and efficient way. One such algorithm is Kadane’s Algorithm, which is used to find the maximum subarray sum of an array of numbers.

The algorithm was first introduced by Jay Kadane in 1984 in his paper “Maximum Sum Subarray Problem.”

### What is Kadane’s Algorithm?
Kadane’s Algorithm is a dynamic programming algorithm used to solve the maximum subarray problem.
The maximum subarray problem is the task of finding the contiguous subarray within a one-dimensional array of numbers that has the largest sum.
The subarray can be of any length, including the entire array. Kadane’s Algorithm works by scanning through the array and keeping track of the current subarray sum, updating it as it goes along.
The algorithm returns the maximum subarray sum found.

### The Uniqueness of Kadane’s Algorithm:
One of the unique features of Kadane’s Algorithm is its simplicity and efficiency.
The algorithm requires only a single scan through the array, making it faster than other approaches to the maximum subarray problem, which may require multiple scans or nested loops.

### How Kadane’s Algorithm works
Kadane’s Algorithm works by keeping track of two variables as it scans through the array: the current subarray sum and the maximum subarray sum seen so far.
The algorithm starts by setting both variables to the value of the first element in the array.
The algorithm then iterates through the array, adding each element to the current subarray sum.
If the current subarray sum becomes negative, the algorithm resets it to zero, effectively discarding any negative subarrays.
The maximum subarray sum seen so far is updated whenever the current subarray sum exceeds it.
### Advantages and Disadvantages:

# Advantages
Kadane’s Algorithm is efficient and requires only a single scan through the array.
The algorithm is simple to understand and implement.
It works well for arrays with both positive and negative numbers.

# Disadvantages
Kadane’s Algorithm only works for arrays with at least one positive number. If all numbers in the array are negative, the algorithm will return 0 as the maximum subarray sum.
The algorithm may not work for arrays with very large or very small values, as it can suffer from overflow or underflow issues.

### Use Cases
Kadane’s Algorithm has many applications in computer science and beyond. Here are some examples:

It can be used to find the maximum subarray sum in a stock price array, helping traders to identify profitable buying and selling opportunities.
It can be used in image processing to find the brightest or darkest subregions of an image.
It can be used in speech recognition to identify the most important or significant parts of a spoken sentence.