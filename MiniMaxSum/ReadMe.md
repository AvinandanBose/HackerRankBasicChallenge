![Screenshot (247)](https://user-images.githubusercontent.com/38869235/220708213-cb08aef1-606b-4713-a0fa-b72ba972457f.png)
![Screenshot (248)](https://user-images.githubusercontent.com/38869235/220708517-3dc23c10-4194-4d8a-ae5a-cae6eb5b26c3.png)

<h3 align="Left">
  
```
  
  Solution:
  
   public static void miniMaxSum(List<Integer> arr) {
     		long min = arr.get(0);
        long max = arr.get(0);
        long sum = 0;
        for (int i = 0; i < arr.size(); i++) {
            if (arr.get(i) < min) {
                min = arr.get(i);
            }
            if (arr.get(i) > max) {
                max = arr.get(i);
            }
            sum += arr.get(i);
        }
        System.out.println((sum - max) + " " + (sum - min));
    }

}
  
Explanation: Later....
  
```
</h3>
