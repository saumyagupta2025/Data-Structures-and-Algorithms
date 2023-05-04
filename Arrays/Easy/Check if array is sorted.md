## Check if the array is sorted

Given an array **arr[]** of size **N**, check if it is sorted in non-decreasing order or not.

**Example 1:**
```
Input:
N = 5
arr[] = {10, 20, 30, 40, 50}
Output: 1
Explanation: The given array is sorted.
```

**Example 2:**

```
Input:
N = 6
arr[] = {90, 80, 100, 70, 40, 30}
Output: 0
Explanation: The given array is not sorted.
```

**Expected Time Complexity:** O(N)  
**Expected Auxiliary Space:** O(1)

**Constraints:**  
1 ≤ N ≤ 105  
1 ≤ Arr[i] ≤ 106

**Approach:**
1.  Initialize a boolean variable `flag` to `True`.
2.  Iterate over the array from the first to the second-to-last element.
3.  For each pair of adjacent elements, compare the current element with the next element.
4.  If the current element is greater than the next element, set `flag` to `False` and exit the loop.
5.  Return the value of `flag`.

**Solution:**
```
class Solution {
    boolean arraySortedOrNot(int[] arr, int n) {
        // code here
        boolean flag = true;
        for (int i = 0; i<n-1; i++){
            if(arr[i]>arr[i+1])
               {
               flag = false;
               break;
               } 
            
        }
        return flag;
    }
}
```