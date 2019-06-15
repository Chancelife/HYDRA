```java
class Solution {    
    public int numTilePossibilities(String tiles) {
        int[] count = new int[26];
        for(char c:tiles.toCharArray())
            count[c-'A']++;
        int ans = 0;
        Queue<int[]> queue = new LinkedList<>();
        int[] temp;
        do {
            if(queue.isEmpty()) temp = count;
            else temp = queue.remove();
            
            for(int i=0;i<26;i++) {
                if(temp[i]!=0) {
                    temp[i]--;
                    queue.add(temp.clone());
                    temp[i]++;
                    ans++;
                }
            }
        } while(!queue.isEmpty());
        return ans;
        
    }
}
```

