```java
class Solution {
    public void rotate(int[] nums, int k) {
        if(k==0) return ;
        if(k>nums.length) k = k%nums.length;
        int[] ans = new int[nums.length];
        int p1, p2 = nums.length-k;
        for(p1=0;p1<nums.length;p1++) {
            if(p2>=nums.length) p2 = 0;
            ans[p1] = nums[p2++];
        }
        System.arraycopy(ans, 0, nums, 0, ans.length);
    }
}
```
#### * time: O(N)
#### * space: O(N)