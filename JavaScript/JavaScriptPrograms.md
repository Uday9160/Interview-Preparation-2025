# Top 30 JavaScript Array Programs for 5+ Years Experience
01. **Reverse an Array**
02. **Find the Largest and Smallest Element in an Array**
03. **Remove Duplicates from an Array**
04. **Find the Intersection of Two Arrays**
05. **Find the Union of Two Arrays**
06. **Rotate an Array by K Positions**
07. **Find All Pairs in an Array with a Given Sum**
08. **Find the Frequency of Each Element in an Array**
09. **Sort an Array Without Using Built-in Sort**
10. **Find the Second Largest/Smallest Element**
11. **Check if Two Arrays are Equal**
12. **Flatten a Nested Array**
13. **Chunk an Array into Smaller Arrays**
14. **Find the Missing Number in a Sequence**
15. **Find the First Non-Repeating Element**
16. **Move All Zeros to the End of the Array**
17. **Find the Longest Increasing Subsequence**
18. **Find the Subarray with the Maximum Sum (Kadane’s Algorithm)**
19. **Group Anagrams from an Array of Strings**
20. **Find All Unique Triplets that Sum to Zero**
21. **Find the Median of Two Sorted Arrays**
22. **Find the Kth Largest Element**
23. **Implement Array Map, Filter, and Reduce**
24. **Find the Duplicate Number in an Array**
25. **Find the Majority Element**
26. **Merge Two Sorted Arrays**
27. **Find the Common Elements in Three Sorted Arrays**
28. **Find the Product of Array Except Self**
29. **Find All Subsets (Power Set) of an Array**
30. **Find the Longest Consecutive Sequence**

### 1. **Reverse an Array**

**Answer:**

**Psudeocode:**

01. Create a new empty array called `reversed`.
02. Loop through the original array from the last element to the first element.
03. In each iteration, push the current element into the `reversed` array.
04. Return the `reversed` array.

**INPUT AND OUTPUT:**

```javascript
input: [1, 2, 3, 4, 5]
output: [5, 4, 3, 2, 1]
```

**ANSWER:**

```javascript
function reverseArray(arr) {
    let reversed = [];
    for (let i = arr.length - 1; i >= 0; i--) {
        reversed.push(arr[i]);
    }
    return reversed;
}
# # # TRACE:
    // Example usage:
    console.log(reverseArray([1, 2, 3, 4, 5])); // Output: [5, 4, 3, 2, 1]
in 1 st iteration i = 4, arr[4] = 5, reversed = [5] in 2n d iteration i = 3, arr[3] = 4, reversed = [5, 4] in 3 rd iteration i = 2, arr[2] = 3, reversed = [5, 4, 3] in 4 th iteration i = 1, arr[1] = 2, reversed = [5, 4, 3, 2] in 5 th iteration i = 0, arr[0] = 1, reversed = [5, 4, 3, 2, 1] in 6 th iteration i = -1, loop ends
```

---

### 2. **Find Maximum Element in Array**

**Answer:**

**Psudeocode:**

01. Initialize a variable `max` with the first element of the array.
02. Loop through the rest of the array.
03. If any element is greater than `max`, update `max`.
04. Return `max`.

**INPUT AND OUTPUT:**

```javascript
input: [3, 9, 1, 6]
output: 9
```

**ANSWER:**

```javascript
function findMax(arr) {
    let max = arr[0];
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}
# # # TRACE:
    // Example usage:
    console.log(findMax([3, 9, 1, 6])); // Output: 9
start: max = 3
i = 1, arr[1] = 9 > max→ max = 9
i = 2, arr[2] = 1 < max→ max = 9
i = 3, arr[3] = 6 < max→ max = 9
loop ends
```

---

### 3. **Find Minimum Element in Array**

**Answer:**

**Psudeocode:**

01. Initialize a variable `min` with the first element.
02. Loop through the array.
03. If current element is less than `min`, update `min`.
04. Return `min`.

**INPUT AND OUTPUT:**

```javascript
input: [5, 2, 8, 1]
output: 1
```

**ANSWER:**

```javascript
function findMin(arr) {
    let min = arr[0];
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] < min) {
            min = arr[i];
        }
    }
    return min;
}
# # # TRACE:
    // Example usage:
    console.log(findMin([5, 2, 8, 1])); // Output: 1
start: min = 5
i = 1, arr[1] = 2 < min→ min = 2
i = 2, arr[2] = 8 > min→ min = 2
i = 3, arr[3] = 1 < min→ min = 1
loop ends
```

---

### 4. **Sum All Elements in Array**

**Answer:**

**Psudeocode:**

01. Initialize `sum` as 0.
02. Loop through the array and add each element to `sum`.
03. Return the sum.

**INPUT AND OUTPUT:**

```javascript
input: [1, 2, 3, 4]
output: 10
```

**ANSWER:**

```javascript
function sumArray(arr) {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum;
}
# # # TRACE:
    // Example usage:
    console.log(sumArray([1, 2, 3, 4])); // Output: 10
sum = 0
i = 0, sum = 0 + 1 = 1
i = 1, sum = 1 + 2 = 3
i = 2, sum = 3 + 3 = 6
i = 3, sum = 6 + 4 = 10
loop ends
```

---

### 5. **Count Occurrences of an Element**

**Answer:**

**Psudeocode:**

01. Initialize `count = 0`.
02. Loop through the array.
03. If element equals target, increment `count`.
04. Return `count`.

**INPUT AND OUTPUT:**

```javascript
input: [1, 2, 3, 2, 2, 4], element = 2
output: 3
```

**ANSWER:**

```javascript
function countOccurrences(arr, target) {
    let count = 0;
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] === target) {
            count++;
        }
    }
    return count;
}
# # # TRACE:
    // Example usage:
    console.log(countOccurrences([1, 2, 3, 2, 2, 4], 2)); // Output: 3
i = 0, arr[0] = 1≠ 2→ count = 0
i = 1, arr[1] = 2 = 2→ count = 1
i = 2, arr[2] = 3≠ 2→ count = 1
i = 3, arr[3] = 2 = 2→ count = 2
i = 4, arr[4] = 2 = 2→ count = 3
i = 5, arr[5] = 4≠ 2→ count = 3
```

---

### 6. **Reverse a String**

**Answer:**

**Psudeocode:**

01. Initialize an empty string `reversed`.
02. Loop over input string from end to start.
03. Append each character to `reversed`.
04. Return `reversed`.

**INPUT AND OUTPUT:**

```javascript
input: "hello"
output: "olleh"
```

**ANSWER:**

```javascript
function reverseString(str) {
    let reversed = "";
    for (let i = str.length - 1; i >= 0; i--) {
        reversed += str[i];
    }
    return reversed;
}
# # # TRACE:
    // Example usage:
    console.log(reverseString("hello")); // Output: "olleh"
i = 4, reversed = "o"
i = 3, reversed = "ol"
i = 2, reversed = "oll"
i = 1, reversed = "olle"
i = 0, reversed = "olleh"
```

---

### 7. **Check if Array is Palindrome**

**Answer:**

**Psudeocode:**

01. Initialize two pointers: start = 0, end = arr.length - 1.
02. While start < end:

   * If arr\[start] != arr\[end], return false.
   * Else increment start, decrement end.
03. Return true.

**INPUT AND OUTPUT:**

```javascript
input: [1, 2, 3, 2, 1]
output: true
```

**ANSWER:**

```javascript
function isPalindrome(arr) {
    for (let i = 0; i < arr.length / 2; i++) {
        if (arr[i] !== arr[arr.length - 1 - i]) {
            return false;
        }
    }
    return true;
}
# # # TRACE:
    // Example usage:
    console.log(isPalindrome([1, 2, 3, 2, 1])); // Output: true
i = 0, arr[0] = 1, arr[4] = 1→ match
i = 1, arr[1] = 2, arr[3] = 2→ match
i = 2, middle→ done
```

---

### 8. **Copy One Array into Another**

**Answer:**

**Psudeocode:**

01. Create empty array `copy`.
02. Loop through original array.
03. Push each element into `copy`.
04. Return `copy`.

**INPUT AND OUTPUT:**

```javascript
input: [10, 20, 30]
output: [10, 20, 30]
```

**ANSWER:**

```javascript
function copyArray(arr) {
    let copy = [];
    for (let i = 0; i < arr.length; i++) {
        copy[i] = arr[i];
    }
    return copy;
}
# # # TRACE:
    // Example usage:
    console.log(copyArray([10, 20, 30])); // Output: [10, 20, 30]
copy[0] = 10, copy[1] = 20, copy[2] = 30
```

---

### 9. **Find Second Largest Element**

**Answer:**

**Psudeocode:**

01. Initialize `largest` and `secondLargest` as -Infinity.
02. Loop through array.
03. If current > largest → update both.
04. Else if current > secondLargest and ≠ largest → update secondLargest.
05. Return `secondLargest`.

**INPUT AND OUTPUT:**

```javascript
input: [10, 5, 8, 20, 15]
output: 15
```

**ANSWER:**

```javascript
function secondLargest(arr) {
    let largest = -Infinity;
    let second = -Infinity;
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] > largest) {
            second = largest;
            largest = arr[i];
        } else if (arr[i] > second && arr[i] !== largest) {
            second = arr[i];
        }
    }
    return second;
}
# # # TRACE:
    // Example usage:
    console.log(secondLargest([10, 5, 8, 20, 15])); // Output: 15
```

---

### 10. **Remove Duplicates From Array Without Set**

**Answer:**

**Psudeocode:**

01. Initialize empty array `unique`.
02. Loop through input array.
03. For each element, check if it's already in `unique`.
04. If not, push to `unique`.
05. Return `unique`.

**INPUT AND OUTPUT:**

```javascript
input: [1, 2, 2, 3, 1]
output: [1, 2, 3]
```

**ANSWER:**

```javascript
function removeDuplicates(arr) {
    let unique = [];
    for (let i = 0; i < arr.length; i++) {
        let found = false;
        for (let j = 0; j < unique.length; j++) {
            if (arr[i] === unique[j]) {
                found = true;
                break;
            }
        }
        if (!found) {
            unique.push(arr[i]);
        }
    }
    return unique;
}
# # # TRACE:
    // Example usage:
    console.log(removeDuplicates([1, 2, 2, 3, 1])); // Output: [1, 2, 3]
```

**11. Check if an Array Contains a Duplicate**
Answer:

Pseudocode:

01. Create an empty set to keep track of seen elements.
02. Iterate through the array.
03. For each element, check if it exists in the set.
04. If yes, return `true`.
05. If not, add the element to the set.
06. After the loop, return `false`.

INPUT AND OUTPUT:

```javascript
input: [1, 2, 3, 4, 2]
output: true
```

ANSWER:

```javascript
function hasDuplicate(arr) {
    let seen = new Set();
    for (let num of arr) {
        if (seen.has(num)) {
            return true;
        }
        seen.add(num);
    }
    return false;
}
# # # TRACE:
// input: [1, 2, 3, 4, 2]
// seen = {}
// num = 1 -> add to seen -> seen = {1}
// num = 2 -> add to seen -> seen = {1,2}
// num = 3 -> add to seen -> seen = {1,2,3}
// num = 4 -> add to seen -> seen = {1,2,3,4}
// num = 2 -> already in seen => return true
```

---

**12. Find All Duplicates in an Array**
Answer:

Pseudocode:

01. Create an object to count occurrences.
02. Iterate through the array and update counts.
03. Iterate the count object and collect keys where value > 1.
04. Return those keys.

INPUT AND OUTPUT:

```javascript
input: [4, 3, 2, 7, 8, 2, 3, 1]
output: [2, 3]
```

ANSWER:

```javascript
function findDuplicates(arr) {
    let count = {};
    let result = [];
    for (let num of arr) {
        count[num] = (count[num] || 0) + 1;
    }
    for (let num in count) {
        if (count[num] > 1) {
            result.push(Number(num));
        }
    }
    return result;
}

# # # TRACE:
// count = {}
// after loop: { '1':1, '2':2, '3':2, '4':1, '7':1, '8':1 }
// result: [2,3]
```

---

**13. Move Zeros to End**
Answer:

Pseudocode:

01. Create a new array for non-zero elements.
02. Count the number of zeros.
03. Append the same number of zeros to the end.
04. Return the new array.

INPUT AND OUTPUT:

```javascript
input: [0, 1, 0, 3, 12]
output: [1, 3, 12, 0, 0]
```

ANSWER:

```javascript
function moveZeros(arr) {
    let nonZero = [];
    let zeroCount = 0;
    for (let num of arr) {
        if (num === 0) zeroCount++;
        else nonZero.push(num);
    }
    while (zeroCount--) {
        nonZero.push(0);
    }
    return nonZero;
}
# # # TRACE:
// nonZero: [1, 3, 12]
// zeroCount: 2
// result: [1, 3, 12, 0, 0]
```

---

**14. Merge Two Sorted Arrays**
Answer:

Pseudocode:

01. Use two pointers starting at 0.
02. Compare elements and push the smaller one.
03. Move the pointer of the array whose element was smaller.
04. After one array ends, add remaining elements of the other.

INPUT AND OUTPUT:

```javascript
input: [1, 3, 5], [2, 4, 6]
output: [1, 2, 3, 4, 5, 6]
```

ANSWER:

```javascript
function mergeSortedArrays(a, b) {
    let result = [];
    let i = 0,
        j = 0;
    while (i < a.length && j < b.length) {
        if (a[i] < b[j]) {
            result.push(a[i++]);
        } else {
            result.push(b[j++]);
        }
    }
    return result.concat(a.slice(i)).concat(b.slice(j));
}
# # # TRACE:
// [1,3,5], [2,4,6]
// i=0,j=0 -> push 1 -> i++
// i=1,j=0 -> push 2 -> j++
// i=1,j=1 -> push 3 -> i++
// i=2,j=1 -> push 4 -> j++
// i=2,j=2 -> push 5 -> i++
// i=3,j=2 -> push 6 -> j++
// done: [1,2,3,4,5,6]
```

---

**15. Find Missing Number from 1 to n**
Answer:

Pseudocode:

01. Calculate expected sum of numbers from 1 to n using formula.
02. Subtract actual sum of the array.
03. The result is the missing number.

INPUT AND OUTPUT:

```javascript
input: [1, 2, 4, 5, 6]
output: 3
```

ANSWER:

```javascript
function findMissing(arr) {
    let n = arr.length + 1;
    let expectedSum = (n * (n + 1)) / 2;
    let actualSum = arr.reduce((a, b) => a + b, 0);
    return expectedSum - actualSum;
}
# # # TRACE:
// n = 6
// expectedSum = 21
// actualSum = 1+2+4+5+6 = 18
// missing = 21 - 18 = 3
```

---

**16. Count Occurrences of Elements**
Answer:

Pseudocode:

01. Create an object.
02. Iterate array and increase count of each element.
03. Return the object.

INPUT AND OUTPUT:

```javascript
input: [1, 2, 2, 3, 1, 1]
output: {
    1: 3,
    2: 2,
    3: 1
}
```

ANSWER:

```javascript
function countOccurrences(arr) {
    let count = {};
    for (let num of arr) {
        count[num] = (count[num] || 0) + 1;
    }
    return count;
}
# # # TRACE:
// [1, 2, 2, 3, 1, 1]
// count = {1:3, 2:2, 3:1}
```

---

**17. Find Union of Two Arrays**
Answer:

Pseudocode:

01. Merge both arrays using spread.
02. Use `Set` to remove duplicates.
03. Convert back to array and return.

INPUT AND OUTPUT:

```javascript
input: [1, 2, 3], [2, 3, 4]
output: [1, 2, 3, 4]
```

ANSWER:

```javascript
function unionArrays(a, b) {
    return [...new Set([...a, ...b])];
}
# # # TRACE:
// merge: [1,2,3,2,3,4]
// set: {1,2,3,4}
// result: [1,2,3,4]
```

---

**18. Find Intersection of Two Arrays**
Answer:

Pseudocode:

01. Convert one array to a set.
02. Iterate other array.
03. If element exists in set, add to result.
04. Return result.

INPUT AND OUTPUT:

```javascript
input: [1, 2, 3], [2, 3, 4]
output: [2, 3]
```

ANSWER:

```javascript
function intersection(a, b) {
    let setB = new Set(b);
    return a.filter(num => setB.has(num));
}
# # # TRACE:
// a: [1,2,3], setB: {2,3,4}
// 1 -> not in setB
// 2 -> in setB
// 3 -> in setB
// result: [2, 3]
```

---

**19. Find Difference of Two Arrays**
Answer:

Pseudocode:

01. Convert second array to a set.
02. Filter elements in first array not in the set.

INPUT AND OUTPUT:

```javascript
input: [1, 2, 3], [2, 3]
output: [1]
```

ANSWER:

```javascript
function difference(a, b) {
    let setB = new Set(b);
    return a.filter(num => !setB.has(num));
}
# # # TRACE:
// a: [1,2,3], setB: {2,3}
// result: [1]
```

---

**20. Rotate Array by K Steps**
Answer:

Pseudocode:

01. Calculate k % array length.
02. Slice last k elements and first n-k elements.
03. Concatenate and return.

INPUT AND OUTPUT:

```javascript
input: [1, 2, 3, 4, 5, 6, 7], k = 3
output: [5, 6, 7, 1, 2, 3, 4]
```

ANSWER:

```javascript
function rotateArray(arr, k) {
    k = k % arr.length;
    return arr.slice(-k).concat(arr.slice(0, -k));
}
# # # TRACE:
// k = 3
// slice(-3): [5,6,7]
// slice(0,-3): [1,2,3,4]
// result: [5,6,7,1,2,3,4]
```

---

---

### **21. Check If Two Arrays Are Equal (Regardless of Order)**

**Pseudocode**

01. If arrays have different lengths, return false.
02. Sort both arrays.
03. Compare each element one by one.
04. If any mismatch, return false.
05. Else, return true.

**Input and Output**

```javascript
input: [1, 2, 3], [3, 2, 1]
output: true
```

**Code**

```javascript
function arraysEqual(a, b) {
    if (a.length !== b.length) return false;
    a.sort((x, y) => x - y);
    b.sort((x, y) => x - y);
    for (let i = 0; i < a.length; i++) {
        if (a[i] !== b[i]) return false;
    }
    return true;
}
```

**Trace**

* Sorted a: \[1, 2, 3]
* Sorted b: \[1, 2, 3]
* Compare each → all match → return true

---

### **22. Check If Two Arrays Are Disjoint (No Common Elements)**

**Pseudocode**

01. Convert one array to a set.
02. Iterate other array.
03. If any element exists in the set, return false.
04. Return true if loop completes.

**Input and Output**

```javascript
input: [1, 2, 3], [4, 5, 6]
output: true
```

**Code**

```javascript
function areDisjoint(a, b) {
    let setA = new Set(a);
    for (let el of b) {
        if (setA.has(el)) return false;
    }
    return true;
}
```

**Trace**

* setA: {1, 2, 3}
* b: 4, 5, 6 → none found → return true

---

### **23. Find Second Largest Number in Array**

**Pseudocode**

01. Initialize `max` and `secondMax` as `-Infinity`.
02. Loop through array:

   * If num > max → update both
   * Else if num > secondMax and num !== max → update secondMax
03. Return secondMax.

**Input and Output**

```javascript
input: [10, 5, 20, 8]
output: 10
```

**Code**

```javascript
function secondLargest(arr) {
    let max = -Infinity,
        secondMax = -Infinity;
    for (let num of arr) {
        if (num > max) {
            secondMax = max;
            max = num;
        } else if (num > secondMax && num !== max) {
            secondMax = num;
        }
    }
    return secondMax;
}
```

**Trace**

* max = 20, secondMax = 10 → return 10

---

### **24. Find Second Smallest Number in Array**

**Pseudocode**

01. Initialize `min` and `secondMin` as `Infinity`.
02. Loop through array:

   * If num < min → update both
   * Else if num < secondMin and num !== min → update secondMin
03. Return secondMin.

**Input and Output**

```javascript
input: [10, 5, 20, 8]
output: 8
```

**Code**

```javascript
function secondSmallest(arr) {
    let min = Infinity,
        secondMin = Infinity;
    for (let num of arr) {
        if (num < min) {
            secondMin = min;
            min = num;
        } else if (num < secondMin && num !== min) {
            secondMin = num;
        }
    }
    return secondMin;
}
```

**Trace**

* min = 5, secondMin = 8 → return 8

---

### **25. Reverse an Array**

**Pseudocode**

01. Use two-pointer approach (start, end).
02. Swap start and end until start >= end.

**Input and Output**

```javascript
input: [1, 2, 3, 4]
output: [4, 3, 2, 1]
```

**Code**

```javascript
function reverseArray(arr) {
    let start = 0,
        end = arr.length - 1;
    while (start < end) {
        [arr[start], arr[end]] = [arr[end], arr[start]];
        start++;
        end--;
    }
    return arr;
}
```

**Trace**

* 1↔4 → \[4, 2, 3, 1]
* 2↔3 → \[4, 3, 2, 1]

---

### **26. Remove Duplicates From Array**

**Pseudocode**

01. Use a Set to automatically filter unique values.
02. Convert set to array and return.

**Input and Output**

```javascript
input: [1, 2, 2, 3, 3, 3]
output: [1, 2, 3]
```

**Code**

```javascript
function removeDuplicates(arr) {
    return [...new Set(arr)];
}
```

**Trace**

* Set: {1, 2, 3} → Array: \[1, 2, 3]

---

### **27. Find First Repeating Element**

**Pseudocode**

01. Create a set to track seen elements.
02. Loop through array.
03. If element exists in set, return it.
04. Else add it to set.

**Input and Output**

```javascript
input: [2, 5, 1, 2, 3]
output: 2
```

**Code**

```javascript
function firstRepeating(arr) {
    let seen = new Set();
    for (let num of arr) {
        if (seen.has(num)) return num;
        seen.add(num);
    }
    return -1;
}
```

**Trace**

* seen: 2 → not in set → add
* seen: 5 → add
* seen: 1 → add
* seen: 2 → already in set → return 2

---

### **28. Check If Array Is Sorted**

**Pseudocode**

01. Loop from i = 0 to n - 2.
02. If any arr\[i] > arr\[i+1], return false.
03. Return true.

**Input and Output**

```javascript
input: [1, 2, 3, 4]
output: true
```

**Code**

```javascript
function isSorted(arr) {
    for (let i = 0; i < arr.length - 1; i++) {
        if (arr[i] > arr[i + 1]) return false;
    }
    return true;
}
```

**Trace**

* 1<2<3<4 → return true

---

### **29. Find Frequency of Each Element**

**Pseudocode**

01. Create a frequency object.
02. Iterate array, update frequency.
03. Return object.

**Input and Output**

```javascript
input: [1, 2, 2, 1, 3]
output: {
    1: 2,
    2: 2,
    3: 1
}
```

**Code**

```javascript
function elementFrequency(arr) {
    let freq = {};
    for (let num of arr) {
        freq[num] = (freq[num] || 0) + 1;
    }
    return freq;
}
```

**Trace**

* freq = {1: 2, 2: 2, 3: 1}

---

### **30. Count Pairs with Given Sum**

**Pseudocode**

01. Use a Map to store count of elements.
02. For each element, check `target - num` in map.
03. Add to count.
04. Update current number in map.

**Input and Output**

```javascript
input: [1, 5, 7, -1, 5], sum = 6
output: 3 // (1,5), (1,5), (7,-1)
```

**Code**

```javascript
function countPairs(arr, target) {
    let map = new Map();
    let count = 0;
    for (let num of arr) {
        let complement = target - num;
        if (map.has(complement)) {
            count += map.get(complement);
        }
        map.set(num, (map.get(num) || 0) + 1);
    }
    return count;
}
```

**Trace**

* (1, 5), (7, -1), another (1, 5) → total = 3

---

---

### **31. Move All Zeroes to End**

**Pseudocode**

01. Create a pointer `i` at 0.
02. Loop through array.
03. If element is not 0, assign it to `arr[i]`, increment `i`.
04. After loop, fill remaining positions with 0.

**Input and Output**

```javascript
input: [0, 1, 0, 3, 12]
output: [1, 3, 12, 0, 0]
```

**Code**

```javascript
function moveZeroes(arr) {
    let i = 0;
    for (let j = 0; j < arr.length; j++) {
        if (arr[j] !== 0) {
            arr[i] = arr[j];
            i++;
        }
    }
    while (i < arr.length) {
        arr[i] = 0;
        i++;
    }
    return arr;
}
```

**Trace**
i=0: arr\[1] = 1 → arr=\[1, 1, 0, 3, 12]
i=1: arr\[3] = 3 → arr=\[1, 3, 0, 3, 12]
i=2: arr\[4] = 12 → arr=\[1, 3, 12, 3, 12]
fill arr\[3]=0, arr\[4]=0 → \[1, 3, 12, 0, 0]

---

### **32. Find All Unique Elements in Array**

**Pseudocode**

01. Create a frequency map.
02. Push elements with count == 1 into result.

**Input and Output**

```javascript
input: [1, 2, 2, 3, 4, 4]
output: [1, 3]
```

**Code**

```javascript
function uniqueElements(arr) {
    let freq = {};
    for (let num of arr) {
        freq[num] = (freq[num] || 0) + 1;
    }
    return Object.keys(freq).filter(key => freq[key] === 1).map(Number);
}
```

**Trace**
freq: {1:1, 2:2, 3:1, 4:2} → filter: 1 and 3

---

### **33. Find the Missing Number in Array of 1 to n**

**Pseudocode**

01. Calculate expected sum = n(n+1)/2
02. Calculate actual sum
03. Missing = expected - actual

**Input and Output**

```javascript
input: [1, 2, 4, 5]
output: 3
```

**Code**

```javascript
function missingNumber(arr) {
    let n = arr.length + 1;
    let total = (n * (n + 1)) / 2;
    let sum = arr.reduce((a, b) => a + b, 0);
    return total - sum;
}
```

**Trace**
n=5, total=15, actual=12 → 15-12 = 3

---

### **34. Count Occurrences of a Number**

**Pseudocode**

01. Loop through array
02. If element equals target, increment count
03. Return count

**Input and Output**

```javascript
input: [1, 2, 2, 3, 2], target: 2
output: 3
```

**Code**

```javascript
function countOccurrences(arr, target) {
    let count = 0;
    for (let num of arr) {
        if (num === target) count++;
    }
    return count;
}
```

**Trace**
count = 3 for number 2

---

### **35. Replace All Occurrences of a Number**

**Pseudocode**

01. Loop through array
02. If element equals `oldVal`, set to `newVal`

**Input and Output**

```javascript
input: [1, 2, 2, 3], replace 2 with 9
output: [1, 9, 9, 3]
```

**Code**

```javascript
function replaceOccurrences(arr, oldVal, newVal) {
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] === oldVal) {
            arr[i] = newVal;
        }
    }
    return arr;
}
```

**Trace**
2 → 9 → arr becomes \[1, 9, 9, 3]

---

### **36. Rotate Array to Right by K Steps**

**Pseudocode**

01. Take last `k` elements → slice(-k)
02. Take first n-k elements → slice(0, n-k)
03. Concatenate both

**Input and Output**

```javascript
input: [1, 2, 3, 4, 5], k = 2
output: [4, 5, 1, 2, 3]
```

**Code**

```javascript
function rotateRight(arr, k) {
    k = k % arr.length;
    return arr.slice(-k).concat(arr.slice(0, arr.length - k));
}
```

**Trace**
last 2: \[4, 5], rest: \[1, 2, 3] → \[4, 5, 1, 2, 3]

---

### **37. Rotate Array to Left by K Steps**

**Pseudocode**

01. Take first `k` elements → slice(0, k)
02. Take rest → slice(k)
03. Concatenate rest + first

**Input and Output**

```javascript
input: [1, 2, 3, 4, 5], k = 2
output: [3, 4, 5, 1, 2]
```

**Code**

```javascript
function rotateLeft(arr, k) {
    k = k % arr.length;
    return arr.slice(k).concat(arr.slice(0, k));
}
```

**Trace**
first 2: \[1, 2], rest: \[3, 4, 5] → \[3, 4, 5, 1, 2]

---

### **38. Find Majority Element (> n/2 times)**

**Pseudocode (Moore's Voting Algorithm)**

01. Set candidate and count.
02. Loop: if count==0, set candidate.
03. If current == candidate → count++ else count--
04. Verify candidate count.

**Input and Output**

```javascript
input: [2, 2, 1, 2, 2]
output: 2
```

**Code**

```javascript
function majorityElement(arr) {
    let count = 0,
        candidate = null;
    for (let num of arr) {
        if (count === 0) candidate = num;
        count += (num === candidate) ? 1 : -1;
    }
    count = 0;
    for (let num of arr) {
        if (num === candidate) count++;
    }
    return count > arr.length / 2 ? candidate : -1;
}
```

**Trace**
Candidate 2 → count=4 → return 2

---

### **39. Merge Two Sorted Arrays**

**Pseudocode**

01. Use two pointers i, j.
02. Compare elements and push smaller into result.
03. Append remaining elements.

**Input and Output**

```javascript
input: [1, 3, 5], [2, 4, 6]
output: [1, 2, 3, 4, 5, 6]
```

**Code**

```javascript
function mergeSorted(a, b) {
    let i = 0,
        j = 0,
        res = [];
    while (i < a.length && j < b.length) {
        if (a[i] < b[j]) res.push(a[i++]);
        else res.push(b[j++]);
    }
    return res.concat(a.slice(i)).concat(b.slice(j));
}
```

**Trace**
1<2 → 1, 2<3 → 2, 3<4 → 3, ... → final = \[1, 2, 3, 4, 5, 6]

---

### **40. Find Intersection of Two Arrays**

**Pseudocode**

01. Convert one array to set.
02. Loop through second array, check presence.
03. Push if not already added.

**Input and Output**

```javascript
input: [1, 2, 2, 3], [2, 2, 4]
output: [2]
```

**Code**

```javascript
function intersection(a, b) {
    let setA = new Set(a);
    let result = new Set();
    for (let num of b) {
        if (setA.has(num)) result.add(num);
    }
    return Array.from(result);
}
```

**Trace**
setA: {1, 2, 3}, check b: 2→add → result = \[2]

---
