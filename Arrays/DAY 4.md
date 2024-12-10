# Rotate Array

This repository contains a solution to the problem of rotating an unsorted array to the left (counter-clockwise direction) by `d` steps, where `d` is a positive integer.

## Problem Statement

Given an unsorted array `arr[]`, the task is to rotate the array to the left (counter-clockwise direction) by `d` steps, where `d` is a positive integer. The rotation should be done in-place.

Note: Consider the array as circular.

### Examples

#### Input 1:
```
arr[] = [1, 2, 3, 4, 5], d = 2
```

#### Output 1:
```
[3, 4, 5, 1, 2]
```
Explanation: When rotated by `2` elements, the array becomes `3 4 5 1 2`.

#### Input 2:
```
arr[] = [2, 4, 6, 8, 10, 12, 14, 16, 18, 20], d = 3
```

#### Output 2:
```
[8, 10, 12, 14, 16, 18, 20, 2, 4, 6]
```
Explanation: When rotated by `3` elements, the array becomes `8 10 12 14 16 18 20 2 4 6`.

#### Input 3:
```
arr[] = [7, 3, 9, 1], d = 9
```

#### Output 3:
```
[3, 9, 1, 7]
```
Explanation: When rotated by `9` times, the array becomes `3 9 1 7`.

## Solution

To rotate the array by `d` steps counter-clockwise:
1. First, compute the effective number of rotations: `d = d % arr.size()`. This accounts for cases where `d` is larger than the size of the array.
2. Reverse the first `d` elements.
3. Reverse the remaining elements from index `d` to the end.
4. Reverse the entire array to get the desired result.

### Code

```cpp
class Solution {
  public:

    // Function to rotate an array by d elements in counter-clockwise direction.
    void rotateArr(vector<int>& arr, int d) {
        d = d % arr.size(); // Handle cases where d > arr.size()
        if (d == 0) {
            return;
        }
        
        // Reverse the first d elements
        reverse(arr.begin(), arr.begin() + d);
        
        // Reverse the remaining elements
        reverse(arr.begin() + d, arr.end());
        
        // Reverse the entire array
        reverse(arr.begin(), arr.end());
    }
};
```

## Time Complexity

- **Time Complexity**: \( O(n) \), where \( n \) is the size of the array. The array is reversed three times, each taking \( O(n) \).
- **Space Complexity**: \( O(1) \), as the operation is performed in-place without using any extra space.

## How to Run the Code

1. Clone this repository to your local machine.
   ```bash
   git clone https://github.com/your-username/rotate-array.git
   ```

2. Navigate to the project directory.
   ```bash
   cd rotate-array
   ```

3. Compile the C++ code:
   ```bash
   g++ -o rotate_array rotate_array.cpp
   ```

4. Run the compiled program:
   ```bash
   ./rotate_array
   ```

## Contributing

Feel free to fork this repository, make changes, and create pull requests. Any suggestions or improvements are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

Make sure to replace `https://github.com/your-username/rotate-array.git` with your actual GitHub repository URL.

This `README.md` provides a brief description of the problem, the solution approach, and the steps to run the code locally.