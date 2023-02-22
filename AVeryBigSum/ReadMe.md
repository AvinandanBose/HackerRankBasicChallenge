<h3 align=Left>
  
```
  
In this challenge, you are required to calculate and print the sum of the elements in an array, 
  keeping in mind that some of those integers may be quite large.

Function Description
------------------------------
Complete the aVeryBigSum function in the editor below. It must return the sum of all array elements.

aVeryBigSum has the following parameter(s):

→int ar[n]: an array of integers .


Return
------------------------
→long: the sum of all array elements


Input Format
------------------------------
The first line of the input consists of an integer n .
The next line contains n space-separated integers contained in the array.

Output Format
----------------------
Return the integer sum of the elements in the array.

Constraints
---------------------
1 ≤ n ≤ 10
0 ≤ ar[i] ≤ 10^10

Sample Input
--------------------
5
1000000001 1000000002 1000000003 1000000004 1000000005

Output
-------------------
5000000015

Note:
------------------------
The range of the 32-bit integer is :
(-21^31)to(2^31-1) or [-2147483648,2147483647]
When we add several integer values, the resulting sum might exceed the above range. 
You might need to use long int C/C++/Java to store such sums.
  
```
</h3>
  
<h3 align=Left>
  
```
Solution
--------------------

Approach : As we are given int ar[n] , 
and each value will be of Long Integer type and each input will add , 
and the resultant value will be also Long type.

Therefore 1st Apprach will be:
public static long aVeryBigSum(List<Long> ar) {
    long sum = 0;
        for (Long aLong : ar) {
            sum += aLong;
        }
        return sum;

    }

}

Using Iterable
-------------
public static long aVeryBigSum(List<Long> ar) {
    Iterable<Long> iterable = ar;
         long sum = 0;
            for (Long i : iterable) {
                sum += i;
            }
            return sum;

    }

}

Using Iterator
-------------
public static long aVeryBigSum(List<Long> ar) {
     Iterator<Long> iterator = ar.iterator();
         long sum = 0;
            while (iterator.hasNext()) {
                sum += iterator.next();
            }
            return sum;

    }

}

And most optimized solution and advanced will be using StreamAPI of Java . 
-----------------------------------------------------------------------
 public static long aVeryBigSum(List<Long> ar) {
    return ar.stream().mapToLong(Long::longValue).sum();

    }

}

Here stream function calls mapToLong function taking each value and 
converting each value by longValue method of wrapper class Long ,
here called by 'method reference ::' 
and add each input by sum() method.





```
</h3>
  
