# sam-part-organizing-team-arranging-university-s-career-fair

[https://www.chegg.com/homework-help/questions-and-answers/sam-part-organizing-team-arranging-university-s-career-fair-list-companies-respective-arri-q39910793](https://www.chegg.com/homework-help/questions-and-answers/sam-part-organizing-team-arranging-university-s-career-fair-list-companies-respective-arri-q39910793)

![](../../.gitbook/assets/image%20%2829%29.png)

## Solution

贪心算法, 计算结束时间, 按照结束时间排序, 每次寻找 开始时间 &gt;= 上次结束时间 并且 最早结束的event

```java
class Solution {

    public int maxEvents(int n, int[] arrival, int[] duration) {
        Map<Integer, Integer> myMap = new TreeMap<>(); // <end time, index>
        for (int i = 0; i < n; i++) { // get a sorted by end time, events index
            if (myMap.get(arrival[i] + duration[i]) != null ) {
                // if end time is duplicated, save the smaller duration
                if (duration[i] < duration[myMap.get(arrival[i] + duration[i])]) {
                    myMap.put(arrival[i] + duration[i], i);
                }
            } else {
                myMap.put(arrival[i] + duration[i], i);
            }
        }
        int scheduledEventsCount = 0;
        int prevIndex = -1;
        for (Integer key : myMap.keySet()) {
            // prev end time <= start time
            if (prevIndex == -1 || 
                (arrival[prevIndex] + duration[prevIndex] <= arrival[myMap.get(key)])) {
                prevIndex = myMap.get(key);
                scheduledEventsCount++;
            } else {
                continue;
            }
        }
        return scheduledEventsCount;
    }
}

public class MainClass {
    
    public static void main(String[] args) throws IOException {
        int n = 5;
        int[] arrival = {1,3,3,5,7};
        int[] duration = {2,2,1,2,1};

        int ret = new Solution().maxEvents(n, arrival, duration);

        System.out.print(ret);
    
    }
}
```

