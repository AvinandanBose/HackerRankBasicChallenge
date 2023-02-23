![Screenshot (260)](https://user-images.githubusercontent.com/38869235/221002067-80bd8c92-d8cb-48c4-9e83-d40771e94412.png)
![Screenshot (261)](https://user-images.githubusercontent.com/38869235/221002316-e66680c3-65e8-4ebe-b2c1-198d351c7c6b.png)
![Screenshot (262)](https://user-images.githubusercontent.com/38869235/221002465-e42c2750-9b1a-4bba-8908-c18faa1562f4.png)
![Screenshot (263)](https://user-images.githubusercontent.com/38869235/221002583-0e00b1ca-de8f-4aea-bb4f-753f6ea65331.png)

<h3>
  
```Syntax
//Not Optimized and TimeOut

 public static int pairs(int k, List<Integer> arr) {
        int count = 0;
        for (int i = 0; i < arr.size(); i++) {
            for (int j = i + 1; j < arr.size(); j++) {
                if (Math.abs(arr.get(i) - arr.get(j)) == k) {
                    count++;
                }
            }
        }
        return count;
        

    } 
  
//Optized Code that run within TimeComplexity:
  
//1st Optimized Code:
 
public static int pairs(int k, List<Integer> arr) {
        
        int count = 0;
        Set<Integer> set = new HashSet<>();
        for (int i : arr) {
            set.add(i);
        }
        for (int i : arr) {
            if (set.contains(i + k)) {
                count++;
            }
        }
        return count;


    }
  
  
// 2nd Optimized Code:
  
 public static int pairs(int k, List<Integer> arr) {
    int count = 0;
        Set<Integer> set = new HashSet<>();
       arr.stream().forEach(set::add);
        for (Integer i : arr) {
            if (set.contains(i + k)) {
                count++;
            }
        }
        return count;
    }
}
 
 // 3rd Optimized Code: 
  
  import java.util.concurrent.atomic.AtomicInteger;

public static int pairs(int k, List<Integer> arr) {
     AtomicInteger count = new AtomicInteger();
        Set<Integer> set = new HashSet<>();
       arr.stream().forEach(set::add);

       arr.stream().forEach(i -> {
           if (set.contains(i + k)) {
               count.getAndIncrement();
           }
       });
        return count.get();
    }
}
  
Explanation : Later....
  
  
```

