import java.util.Arrays;

class Solution {
    public int findContentChildren(int[] g, int[] s) {
        // Sorting both greed factors with their sizes
        Arrays.sort(g);
        Arrays.sort(s);

        int i = 0; // child
        int j = 0; // cookies
        int contentChildren = 0; // count of satisfied children

        // 
        while (i < g.length && j < s.length) {
          
            if (s[j] >= g[i]) {
                contentChildren++;
                i++; 
            }
        
            j++;
        }

        return contentChildren;
    }
}
