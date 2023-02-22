![Screenshot (246)](https://user-images.githubusercontent.com/38869235/220694650-9a0011db-219c-4260-bb32-e78e9e94926b.png)


<h3 align= "Left">

```
This is just a program of pattern.

public static void staircase(int n) {
     for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                if (j <= n - i) {
                    System.out.print(" ");
                } else {
                    System.out.print("#");
                }
            }
            System.out.println();
        }

    }

}

if n=4, Then:
For i = 1
    j = 1
     if(j(1)<=4-1=3)= True
      Hence print = " "[Blank Space] 
      
      if(j(2)<=4-1=3)= True
      Hence print =" "[Blank Space] 
      
      if(j(3)<=4-1=3)= True
      Hence print = " "[Blank Space] 
      
      if(j(4)<=4-1=3)= False
      Hence print = #
      
For i = 1      
    j = 2
      if(j(1)<=4-2=2)= True
      Hence print = " "[Blank Space] 
      
      if(j(2)<=4-2=2)= True
      Hence print =" "[Blank Space] 
      
      if(j(3)<=4-2=2)= False
      Hence print = # 
      
      if(j(4)<=4-2=2)= False
      Hence print = #
 
 Likewise it will continue till 
 i=4
      
      


```
</h3>


