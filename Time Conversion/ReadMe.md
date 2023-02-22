![Screenshot (251)](https://user-images.githubusercontent.com/38869235/220717500-a39c2ed3-190e-4514-a1a7-c48412ed144a.png)
![Screenshot (252)](https://user-images.githubusercontent.com/38869235/220717662-e3df697c-9473-4dce-ae22-55581e97fa8b.png)
![Screenshot (253)](https://user-images.githubusercontent.com/38869235/220717979-213c1456-c4de-47fd-a479-6e028e36f11d.png)


<h3 align="Left">
  
```
Solution:
  
  public static String timeConversion(String s) {
      String[] time = s.split(":");
        String hour = time[0];
        String min = time[1];
        String sec = time[2].substring(0, 2);
        String ampm = time[2].substring(2, 4);
        if (ampm.equals("PM")) {
            if (hour.equals("12")) {
                hour = "12";
            } else {
                hour = String.valueOf(Integer.parseInt(hour) + 12);
            }
        } else {
            if (hour.equals("12")) {
                hour = "00";
            }
        }
        return hour + ":" + min + ":" + sec;

    }

}
  
```
</h3>
  
