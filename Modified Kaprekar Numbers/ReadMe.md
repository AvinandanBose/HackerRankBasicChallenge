![Screenshot (271)](https://user-images.githubusercontent.com/38869235/221277168-b8b0afb5-df90-46fc-b909-70b235ad9a07.png)
![Screenshot (272)](https://user-images.githubusercontent.com/38869235/221277354-51c13a2a-3a6f-4f0c-ae16-ef3aacdfea37.png)
![Screenshot (273)](https://user-images.githubusercontent.com/38869235/221277414-b8d10f29-320f-4797-85a7-7aede93ca1ed.png)

<h3 align="Left">
  
```
  
  public static boolean isKaprekar(long a) {
        long square = a * a;
        String s = String.valueOf(square);
        int len = s.length();
        long left = 0;
        long right = 0;
        if(len == 1) {
            right = square;
        } else {
            left = Long.parseLong(s.substring(0, len / 2));
            right = Long.parseLong(s.substring(len / 2));
        }
        return left + right == a;
    }
    
    public static void kaprekarNumbers(int p, int q) {
   boolean found = false;
        for(int i = p; i <= q; i++) {
            if(isKaprekar(i)) {
                System.out.print(i + " ");
                found = true;
            }
        }
        if(!found) {
            System.out.println("INVALID RANGE");
        }
    }
}

```
</h3>
