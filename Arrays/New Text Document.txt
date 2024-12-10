---

# Second Largest Element in Array

This repository contains a C++ solution to find the second largest element in an array of positive integers. If the second largest element does not exist, the function returns `-1`.

## Problem Description

Given an array of positive integers, the goal is to return the second largest element from the array. If the second largest element doesn't exist (either because all elements are the same or there aren't enough distinct elements), return `-1`.

### Example 1:
**Input**:  
`arr[] = [12, 35, 1, 10, 34, 1]`  
**Output**:  
`34`  
**Explanation**:  
The largest element is `35` and the second largest element is `34`.

### Example 2:
**Input**:  
`arr[] = [10, 5, 10]`  
**Output**:  
`5`  
**Explanation**:  
The largest element is `10` and the second largest element is `5`.

### Example 3:
**Input**:  
`arr[] = [10, 10, 10]`  
**Output**:  
`-1`  
**Explanation**:  
The largest element is `10`, and there is no distinct second largest element.

## Function Signature

```cpp
int getSecondLargest(vector<int> &arr);
```

## Approach

1. **Input Validation**:  
   - If the array has fewer than two elements, return `-1`.

2. **Sorting**:  
   - Sort the array in ascending order.
   
3. **Remove Duplicates**:  
   - Use `std::unique` to remove duplicates from the array.

4. **Check for Second Largest Element**:  
   - If after removing duplicates, there are fewer than two distinct elements, return `-1`.
   - Otherwise, return the second largest element (second-to-last in the array).

## Time Complexity

- Sorting the array takes `O(n log n)`, where `n` is the size of the array.
- Removing duplicates using `std::unique` and `erase` takes `O(n)`.
- The total time complexity is `O(n log n)` due to the sorting step.

## Code

```cpp
#include <algorithm>
#include <vector>
using namespace std;

class Solution {
public:
    int getSecondLargest(vector<int> &arr) {
        int n = arr.size();
        if (n < 2) {
            return -1;
        }
        
        // Sort the array in ascending order
        sort(arr.begin(), arr.end());
        
        // Remove duplicates
        auto last = unique(arr.begin(), arr.end());
        arr.erase(last, arr.end());
        
        int s = arr.size();
        
        // If there are less than 2 distinct elements, return -1
        if (s < 2) {
            return -1;
        }
        
        // Return the second largest element
        return arr[s - 2];
    }
};
```

## How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/repository-name.git
   ```

2. Navigate to the project folder:
   ```bash
   cd repository-name
   ```

3. Compile the C++ code using a C++ compiler (e.g., `g++`):
   ```bash
   g++ -o second_largest main.cpp
   ```

4. Run the program:
   ```bash
   ./second_largest
   ```

## Contributions

Feel free to open issues or submit pull requests for improvements or bug fixes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

This template assumes you already have the C++ code file named `main.cpp` (or something similar). Replace `repository-name` and `yourusername` with your actual GitHub repository name and username. Let me know if you'd like to customize this further!
