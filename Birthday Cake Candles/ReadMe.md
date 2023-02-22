![Screenshot (249)](https://user-images.githubusercontent.com/38869235/220712246-ad59a17b-4412-4605-939e-315b4a5efb31.png)
![Screenshot (250)](https://user-images.githubusercontent.com/38869235/220712409-61cd2202-4617-4fb1-98d9-53a56b551391.png)


<h3 align="Left">
  
```
  Solution:
  
  public static int birthdayCakeCandles(List<Integer> candles) {
    int max = 0;
        int count = 0;
        for (int i = 0; i < candles.size(); i++) {
            if (candles.get(i) > max) {
                max = candles.get(i);
                count = 1;
            } else if (candles.get(i) == max) {
                count++;
            }
        }
        return count;

    }

}
  
  Explanation: Later....
  
```
  
</h3>
