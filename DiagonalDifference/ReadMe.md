<h3 align="Left">

```
Diagonal Difference
-----------------------

Given a square matrix, calculate the absolute difference between the sums of its diagonals.

For example, the square matrix arr  is shown below:

1 2 3
4 5 6
9 8 9

The left-to-right diagonal =1 + 5+ 9 = 15 . The right to left diagonal = 3+5+9=17 . 
Their absolute difference is :|15-17|=2.

Function description
---------------------------------
Complete the  function in the editor below.

diagonalDifference takes the following parameter:

→int arr[n][m]: an array of integers

Return
---------------
→int: the absolute diagonal difference

Input Format
--------------------
The first line contains a single integer,n , the number of rows and columns in the square matrix arr.
Each of the next n lines describes a row, arr[i], and consists of n space-separated integers arr[i][j].


Constraints
-------------------
-100 ≤ arr[i][j] ≤ 100

Output Format
----------------------
Return the absolute difference between the sums of the matrix's two diagonals as a single integer.

Sample Input
---------------------
3
11 2 4
4  5  6
10 8 -12


Sample Output
--------------------
15

Explanation
------------------------
The primary diagonal is:

11
   5
     -12

Sum across the primary diagonal: 11 + 5 - 12 = 4

     4
   5
10

Sum across the secondary diagonal: 4 + 5 + 10 = 19
Difference: |4 - 19| = 15

Note: |x| is the absolute value of x
  
  
```
  
</h3>


<h3 align="Left">

```
Solution:

This is the first approach:
------------------------------------------------------
public static int diagonalDifference(List<List<Integer>> arr) {
       
        int sum1 = 0;
        int sum2 = 0;
        int n = arr.size();
        for (int i = 0; i < n; i++) {
            sum1 += arr.get(i).get(i);
            sum2 += arr.get(i).get(n - i - 1);
        }
        return Math.abs(sum1 - sum2);

    }
 --------------------------------------------   
Here:

Say: 

public static void main(String[] args) {
        List<List<Integer>> arr = new ArrayList<>();
        arr.add(new ArrayList<>(Arrays.asList(11, 2, 4)));
        arr.add(new ArrayList<>(Arrays.asList(4, 5, 6)));
        arr.add(new ArrayList<>(Arrays.asList(10, 8, -12)));
           System.out.println(diagonalDifference(arr));

    }
    
 Matrix:
 
    | 11 2 4 |
    | 4  5 6 |
    | 10 8 -12 |
    
int n = arr.size() ; =3 i.e. 0,1,2 = no. of rows
    
 for (int i = 0; i < n; i++) {
            sum1 += arr.get(i).get(i);
            sum2 += arr.get(i).get(n - i - 1);
            
            i.e.
            
            For sum1
            ---------------
           arr.get(0 [row=0]).get(0 [column=0]) =11 
           Hence : sum1=0 = 0+11 = 11
           
           arr.get(1 [row=1]).get(1 [column=1]) =5 
           Hence : sum1=11 = 11+5 = 16
           
           arr.get(2 [row=2]).get(2 [column=2]) =-12
           Hence : sum1=16 = 16+(-12) = 4
           
           
           For sum2
            ---------------
            arr.get(0 [row=0]).get((n-1)-i[column=(3-1)=2-0 =2 ]) =4
           Hence : sum2=0 = 0+4 = 4
           
           arr.get(1 [row=1]).get((n-1)-i[column=(3-1)=2-1 =1 ]) = 5 
           Hence : sum2=4 = 4+5 = 9
           
           arr.get(2 [row=2]).get((n-1)-i[column=(3-1)=2-2 =0 ])=10
           Hence : sum2=9 = 9+10 = 19
           
           
        }
        
        Return:
        
        Math.abs(4 - 19)
        =Math.abs(-15)
        =15
        
        
 And most using the same idea we can more optimize the code using stream:
 ------------------------------------------------------------------
  public static int diagonalDifference(List<List<Integer>> arr) {
   int n = arr.size();
       return Math.abs(arr.stream().mapToInt(l -> l.get(arr.indexOf(l)) -
       l.get(n - 1 - arr.indexOf(l)) ).sum());

    }
    -------------------------------------------------

        
    
    


```

</h3>
