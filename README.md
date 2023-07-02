 * @param {number[]} nums - The input array of integers.
 */
function moveZeroes(nums) {
  let insertIndex = 0;

  // Move all non-zero elements to the beginning of the array
  for (let i = 0; i < nums.length; i++) {
    if (nums[i] !== 0) {
      nums[insertIndex] = nums[i];
      insertIndex++;
    }
  }

  // Fill the remaining positions with zeroes
  for (let i = insertIndex; i < nums.length; i++) {
    nums[i] = 0;
  }
}

// Test cases
const nums1 = [0, 1, 0, 3, 12];
moveZeroes(nums1);
console.log(nums1); // Output: [1, 3, 12, 0, 0]

const nums2 = [0];
moveZeroes(nums2);
console.log(nums2); // Output: [0]

