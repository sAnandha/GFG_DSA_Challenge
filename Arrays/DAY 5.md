# Next Permutation

This repository contains a solution to the problem of finding the next permutation of an array. The task is to rearrange the elements of the given array into the lexicographically next greater permutation. If no such permutation exists, the array should be rearranged into the lowest possible order (i.e., sorted in ascending order).

## Problem Statement

Given an array `arr[]` representing a permutation, implement the next permutation that rearranges the numbers into the lexicographically next greater permutation. If no such permutation exists, rearrange the numbers into the lowest possible order.

A permutation of an array of integers refers to a specific arrangement of its elements in a sequence or linear order.

### Examples

#### Input 1:
```
arr = [2, 4, 1, 7, 5, 0]
```

#### Output 1:
```
[2, 4, 5, 0, 1, 7]
```
Explanation: The next permutation of the given array is `[2, 4, 5, 0, 1, 7]`.

#### Input 2:
```
arr = [3, 2, 1]
```

#### Output 2:
```
[1, 2, 3]
```
Explanation: As `arr[]` is the last permutation, the next permutation is the lowest one, which is `[1, 2, 3]`.

#### Input 3:
```
arr = [3, 4, 2, 5, 1]
```

#### Output 3:
```
[3, 4, 5, 1, 2]
```
Explanation: The next permutation of the given array is `[3, 4, 5, 1, 2]`.

## Solution

To find the next permutation of an array:
1. Find the largest index `i` such that `arr[i] < arr[i + 1]`. If no such index exists, the array is the last permutation, and we return the smallest permutation (sorted array).
2. Find the largest index `j` such that `arr[i] < arr[j]`.
3. Swap the values of `arr[i]` and `arr[j]`.
4. Reverse the subarray starting from `i + 1` to the end of the array to get the next permutation.

In this solution, we use the standard library function `next_permutation` to efficiently get the next permutation.

### Code

```cpp
class Solution {
  public:
    void nextPermutation(vector<int>& arr) {
        // Find the next permutation using next_permutation function
        next_permutation(arr.begin(), arr.end());
    }
};
```

## Time Complexity

- **Time Complexity**: \( O(n) \), where \( n \) is the size of the array. The `next_permutation` function has a linear time complexity in the worst case.
- **Space Complexity**: \( O(1) \), as the operation is performed in-place without using extra space.

## How to Run the Code

1. Clone this repository to your local machine.
   ```bash
   git clone https://github.com/your-username/next-permutation.git
   ```

2. Navigate to the project directory.
   ```bash
   cd next-permutation
   ```

3. Compile the C++ code:
   ```bash
   g++ -o next_permutation next_permutation.cpp
   ```

4. Run the compiled program:
   ```bash
   ./next_permutation
   ```

## Contributing

Feel free to fork this repository, make changes, and create pull requests. Any suggestions or improvements are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

Make sure to replace `https://github.com/your-username/next-permutation.git` with your actual GitHub repository URL.

This `README.md` provides a brief description of the problem, solution approach, and steps to run the code locally.