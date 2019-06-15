```java
class Solution {
    public List<Integer> getRow(int rowIndex) {
        List<Integer> ans = new ArrayList<>();
        ArrayList<Integer> prev = new ArrayList<>();
        
        ans.add(1);
        for(int i=1;i<rowIndex+1;i++) {
            if(i==1)
                ans.add(1);
            else {
                for(int j=1;j<i;j++) {
                    ans.set(j, prev.get(j-1)+prev.get(j));
                }
                ans.add(1);
            }
            prev = new ArrayList(ans);
        }
        return ans;
    }
}
```

##### * Time: O(N)
##### * Space: O(row+row-1) // use some extra space