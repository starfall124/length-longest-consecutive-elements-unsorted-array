# length-longest-consecutive-elements-unsorted-array

Run this script

```bash
$ node index.js
```
All inputs are hard-coded in the following way:

```javascript
/* index.js */

let nums = [100, 4, 200, 1, 3, 2];
console.log("Input = [" + nums + "]\n");
console.log("-----------------Result--------------------");
console.log("Output = " + longestConsecutiveLength(nums));
console.log("-------------------------------------------");

```
# Steps to solve this problem

1. Return `0` if the given array is empty.
2. Declare five variables, `map`, `max`, `start`, `end`, and `num`, and set them `{}`, `0`, `0`, `0`, and `0`, respectively.
3. Use a for loop with index `i` and copy the value of the number with index `i` to the `num`.
4. Check if the `num` property of `map` object is defined or undefined.
5. If undefined,
   5-1. If `num - 1` property of `map` object is defined, assign `map[num - 1].start` to `start` else assign `num` to `start`.
   
   5-2. If `num + 1` property of `map` object is defined, assign `map[num + 1].end` to `end` else assign `num` to `end`.
   
   5-3. Assign `{start:num, end:num}` to `num` property of `map` object.
   
   5-4. Assign `end` to `map[start].end`.
   
   5-5. Assign `start` to `map[end].start`.
   
   5-6. Assign max value of `end - start + 1` and `max` to `max`
   
6. If defined, skip the current loop.
7. After the loop finishes, return the length of the longest consecutive elements array, which equals to `max`

# Complexity:
- Time complexity of the above algorithm is O(n) because we are iterating over the input array only once and n is the total number of elements in that array. 
- Constant space is O(n), because we are using extra space.
