# leetcode-solution-in-java
# 2825. Make String a Subsequence Using Cyclic Increments(daily challenge)

class Solution {
    public boolean canMakeSubsequence(String s1, String s2) {
        int i = 0;
        int j = 0;
        while (i < s1.length() && j < s2.length()){
            int re = s2.charAt(j)-'a';
            int cur = s1.charAt(i)-'a';
            if (cur == re || re == (cur+1)%26){
                j++;
            }
            i++;
        }
        return j == s2.length();
        
    }
}
