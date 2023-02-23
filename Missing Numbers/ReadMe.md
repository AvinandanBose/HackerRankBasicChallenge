![Screenshot (254)](https://user-images.githubusercontent.com/38869235/220998358-8e8adb04-f5c7-4061-8411-76cf50ed082b.png)
![Screenshot (255)](https://user-images.githubusercontent.com/38869235/220998559-92e3f9fe-6e8d-42f0-b0ff-8e4104148840.png)
![Screenshot (259)](https://user-images.githubusercontent.com/38869235/220998778-731e6ab1-15ed-4a39-a206-38c1a8e18b6b.png)
![Screenshot (257)](https://user-images.githubusercontent.com/38869235/220998975-364f978f-4290-48ee-b09f-a6d0cd2e0eab.png)
![Screenshot (258)](https://user-images.githubusercontent.com/38869235/220999065-0db90b70-004c-4d06-ad98-7bd0ea2f3feb.png)


<h3>
  
```
  
  Solution:
  
  public static List<Integer> missingNumbers(List<Integer> arr, List<Integer> brr) {
    List<Integer> result = new ArrayList<>();
        Map<Integer, Integer> map = new HashMap<>();
        for (Integer i : brr) {
            map.put(i, map.getOrDefault(i, 0) + 1);
        }
        for (Integer i : arr) {
            map.put(i, map.get(i) - 1);
        }
        for (Integer i : map.keySet()) {
            if (map.get(i) > 0) {
                result.add(i);
            }
        }
        return result;

    }

    

}
  
  Explanation : later....
  
```
  
</h3>
