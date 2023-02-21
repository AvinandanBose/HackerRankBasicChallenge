<h3 align="Left">

```
  
Given an array of integers, find the sum of its elements.

For example, if the array array ar=[1,2,3], 1+2+3=6 , so return 6.
  
Function Description
---------------------------
  
Complete the simpleArraySum function in the editor below. 
  It must return the sum of the array elements as an integer.

simpleArraySum has the following parameter(s):

ar: an array of integers
  
Input Format
-----------------------
The first line contains an integer, n, denoting the size of the array.
The second line contains n space-separated integers representing the array's elements.
  
Constraints
-------------
0<n,ar[i]<=1000
 
Output Format
------------------
Print the sum of the array's elements as a single integer.
  
Sample Input
-------------------
6
1 2 3 4 10 11
  
Sample Output
--------------
31
  
Explanation
-------------
We print the sum of the array's elements: 1+2+3+4+10+11
  
  
```
  
</h3>


<h3 align="Left">

```
---------------------
Solution 1: 
--------------------------  
public static int simpleArraySum(List<Integer> ar) { 
int sum = 0;
        for (int i = 0; i < ar.size(); i++) {
            sum += ar.get(i); 
        }
        return sum;

    }
}
--------------------------                                      
Solution 2:
---------------------
 public static int simpleArraySum(List<Integer> ar) {
 Iterator<Integer> it = ar.iterator();
        int sum = 0;
        while (it.hasNext()) {
            sum += it.next();
        }
        return sum;

    }
}
----------------------- 
Solution 3:
----------------------------  
 public static int simpleArraySum(List<Integer> ar) {
 Iterable<Integer> iterable = ar;
        int sum = 0;
        for (Integer i : iterable) {
            sum += i;
        }
        return sum;
    }
}

  
```
</h3>
