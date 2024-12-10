# Move All Zeroes to End

This repository contains a solution to the problem of moving all zero elements to the end of an array while maintaining the order of the non-zero elements.

## Problem Statement

Given an array `arr[]`, the task is to push all the zeros of the given array to the right end while maintaining the order of non-zero elements. The operation must be done in-place.

### Examples

#### Input 1:
```
arr[] = [1, 2, 0, 4, 3, 0, 5, 0]
```

#### Output 1:
```
[1, 2, 4, 3, 5, 0, 0, 0]
```
Explanation: There are three `0`s that are moved to the end.

#### Input 2:
```
arr[] = [10, 20, 30]
```

#### Output 2:
```
[10, 20, 30]
```
Explanation: No change in the array as there are no zeros.

#### Input 3:
```
arr[] = [0, 0]
```

#### Output 3:
```
[0, 0]
```
Explanation: No change in the array as there are all zeros.

## Solution

The approach to solve the problem is as follows:

1. Traverse through the array using a pointer.
2. Whenever a non-zero element is encountered, swap it with the first zero element encountered before it.
3. Continue this until the entire array is traversed.

### Code

```cpp
class Solution {
  public:
    void pushZerosToEnd(vector<int>& arr) {
        int s = arr.size();
        int l = 0;
        
        // Iterate through the array
        for (int i = 0; i < s; i++) {
            if (arr[i] != 0) {
                // Swap non-zero elements with zeros
                swap(arr[i], arr[l]);
                l++;
            }
        }
    }
};
```

## Time Complexity

- **Time Complexity**: \( O(n) \), where \( n \) is the size of the array.
- **Space Complexity**: \( O(1) \), as we are doing the operation in-place without using any extra space.

## How to Run the Code

1. Clone this repository to your local machine.
   ```bash
   git clone https://github.com/your-username/move-zeros-to-end.git
   ```

2. Navigate to the project directory.
   ```bash
   cd move-zeros-to-end
   ```

3. Compile the C++ code:
   ```bash
   g++ -o move_zeros move_zeros.cpp
   ```

4. Run the compiled program:
   ```bash
   ./move_zeros
   ```

## Contributing

Feel free to fork this repository, make changes, and create pull requests. Any suggestions or improvements are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

Make sure to replace `https://github.com/your-username/move-zeros-to-end.git` with your actual GitHub repository URL.
