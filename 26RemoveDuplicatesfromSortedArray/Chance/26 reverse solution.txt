···java
    public void rotate(int[] nums, int k) {
        int len = nums.length;      // [1,2,3,4,5,6,7]
        if(k>nums.length) k = k%len;
        reverse(nums, 0, len-1);    // [7,6,5,4,3,2,1]
        reverse(nums, 0, k-1);      // [5,6,7,4,3,2,1]
        reverse(nums, k, len-1);    // [5,6,7,1,2,3,4]
    }
    
    public void reverse(int[] nums, int start, int end) {
        while(start<end) {
            nums[start] = nums[start]^nums[end];
            nums[end] = nums[start]^nums[end];
            nums[start] = nums[start++]^nums[end--];
        }
    }
```

##### Time: O(N)
##### Space: O(1)