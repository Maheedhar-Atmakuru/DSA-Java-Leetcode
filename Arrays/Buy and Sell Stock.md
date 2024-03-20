
### Optimized solution
```
class Solution {
    public int maxProfit(int[] prices) {
        int ans= 0;
        int currentProfit = 0;
        int minSoFar = prices[0];
        for (int i=1;i<prices.length;i++){
            currentProfit= prices[i]-minSoFar;
            if (currentProfit > ans){
                ans = currentProfit;
            }
            minSoFar =Math.min(minSoFar,prices[i]);
        }
        return ans;
}
}
```

### My initial Solution

```
class Solution {
    public int maxProfit(int[] prices) {
        int max = 0;
        int currentMax;
        for (int i =0;i < (prices.length -1);i++){
            currentMax = prices[i];
            for (int j=i+1;j< prices.length;j++){
                if ((prices[j]-currentMax) > max){
                    max = prices[j]-currentMax;
                }
            }
        }
        return max;
}
}

```

### Learnings 

Examine the test cases carefully to get more insights.
Try to get solution in lesser loops