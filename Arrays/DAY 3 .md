# Reverse an Array

This repository contains a solution to the problem of reversing an array of integers in-place.

## Problem Statement

Given an array `arr[]`, the task is to reverse the given array.

### Examples

#### Input 1:
```
arr = [1, 4, 3, 2, 6, 5]
```

#### Output 1:
```
[5, 6, 2, 3, 4, 1]
```
Explanation: The elements of the array are `1 4 3 2 6 5`. After reversing the array, the first element goes to the last position, the second element goes to the second last position, and so on. Hence, the answer is `5 6 2 3 4 1`.

#### Input 2:
```
arr = [4, 5, 2]
```

#### Output 2:
```
[2, 5, 4]
```
Explanation: The elements of the array are `4 5 2`. The reversed array will be `2 5 4`.

#### Input 3:
```
arr = [1]
```

#### Output 3:
```
[1]
```
Explanation: The array has only a single element, hence the reversed array is the same as the original.

## Solution

The approach to solve the problem is as follows:

1. Use two pointers, `l` and `r`, initially pointing to the first and last elements of the array, respectively.
2. Swap the elements at the `l` and `r` positions.
3. Increment `l` and decrement `r`, and repeat the process until `l` is no longer less than `r`.

### Code

```cpp
class Solution {
  public:
    void reverseArray(vector<int> &arr) {
        int l = 0;
        int r = arr.size() - 1;
        
        // Reverse the array using two pointers
        while (l < r) {
            swap(arr[l], arr[r]);
            l++;
            r--;
        }
    }
};
```

## Time Complexity

- **Time Complexity**: \( O(n) \), where \( n \) is the size of the array. We are traversing the array once.
- **Space Complexity**: \( O(1) \), as we are doing the operation in-place without using any extra space.

## How to Run the Code

1. Clone this repository to your local machine.
   ```bash
   git clone https://github.com/your-username/reverse-array.git
   ```

2. Navigate to the project directory.
   ```bash
   cd reverse-array
   ```

3. Compile the C++ code:
   ```bash
   g++ -o reverse_array reverse_array.cpp
   ```

4. Run the compiled program:
   ```bash
   ./reverse_array
   ```

## Contributing

Feel free to fork this repository, make changes, and create pull requests. Any suggestions or improvements are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

Make sure to replace `https://github.com/your-username/reverse-array.git` with your actual GitHub repository URL.

This README provides a brief description of the problem, solution, and steps to run the code locally.