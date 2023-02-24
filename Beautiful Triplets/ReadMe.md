![Screenshot (274)](https://user-images.githubusercontent.com/38869235/221279052-10c87fb9-6fa6-4c23-8a43-7bf217ae501d.png)
![Screenshot (275)](https://user-images.githubusercontent.com/38869235/221279064-43bfbf06-7106-4e53-90b0-4244bcf58987.png)
![Screenshot (276)](https://user-images.githubusercontent.com/38869235/221279068-d74083bf-8014-44ff-94e6-9b7dede82e1c.png)

![Screenshot (277)](https://user-images.githubusercontent.com/38869235/221279345-ac03019d-f755-4e97-bbff-70c82f1e9b8a.png)
![Screenshot (278)](https://user-images.githubusercontent.com/38869235/221279357-4bf355f4-4be8-41f7-971c-f2240b7702c4.png)

<h3 align="Left">
  
```
  
  Solution:

    public static int beautifulTriplets(int d, List<Integer> arr) {
       int count = 0;
        for (int i = 0; i < arr.size(); i++) {
            for (int j = i + 1; j < arr.size(); j++) {
                if (arr.get(j) - arr.get(i) == d) {
                    for (int k = j + 1; k < arr.size(); k++) {
                        if (arr.get(k) - arr.get(j) == d) {
                            count++;
                        }
                    }
                }
            }
        }
        return count;

    }  
  
```
</h3>
