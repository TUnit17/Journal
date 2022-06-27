```
/*

Example
==============
1)
             [     0        1          2         3        4   ]  
wordsDict = ["practice", "makes", "perfect", "coding", "makes"], 
word1 = "coding", word2 = "practice"
res = 3

coding appears 1x
practice appears 1x

2)
                    [     0        1          2         3        4   ]        
Input: wordsDict = ["practice", "makes", "perfect", "coding", "makes"], 
word1 = "makes", word2 = "coding"
Output: 1

makes appears 2x
coding appears 1x


*/

class Solution {
    public int shortestDistance(String[] wordsDict, String word1, String word2) {
        int index1 = Integer.MAX_VALUE;
        int index2 = Integer.MAX_VALUE;
        int min =  Integer.MAX_VALUE;
        
        for(int i=0; i<wordsDict.length; i++){
            if(wordsDict[i].equals(word1)){
                index1 = i;
                int curr = Math.abs(index1-index2);
                min = Math.min(min, curr);
            }
            else if(wordsDict[i].equals(word2)){
                index2 = i;
                int curr = Math.abs(index1-index2);
                min = Math.min(min, curr);
            }
        }  
        return min;
    }
}

```
