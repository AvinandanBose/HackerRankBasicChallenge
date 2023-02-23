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
  
Explanation: Acctording the question given :

1st Approach:

As we have the inputs from the given Test Cases :
We have to find the minimum and maximum number from 
the given inputs, as per the condition.

Suppose we have : 1, 2,3,4,5 = Max: 5 and Min:1

Add other numbers with MIN excluding MAX:
1+2+3+4 = 10

Add other numbers with MAX excluding MIN:
2+3+4+5 = 14

Which can also be acieved by following program:

public static void miniMaxSum(List<Integer> arr) {
        List<Integer> arr1 = arr;//Taking to another array
        List<Integer> arr2 = arr;//Taking to another array 
        long min = arr.get(0);
        long max = arr.get(0);
    
    //Getting MIN and MAX
        for (int i = 0; i < arr.size(); i++) {
            if (arr.get(i) < min) {
                min = arr.get(i);
            }
            if (arr.get(i) > max) {
                max = arr.get(i);
            }
        }
        long sum1 = 0;
        long sum2 = 0;
        
        //For 1st Sum
        for (int i = 0; i < arr1.size(); i++) {
            if(arr1.get(i)==min){
                
                //SKIP
                continue;

            }
            else{
                sum1 += arr1.get(i);
            }

        }
        
         //For 2nd Sum
        for (int i = 0; i < arr2.size(); i++) {
            if(arr1.get(i)==max){
            
                //SKIP
                continue;

            }
            sum2 += arr2.get(i);
        }

        System.out.println(sum2 + " " + sum1);
    }
}

But the as the program gets lengthy and with high line of codes,
It may fail to most of the test cases , hence :

There is a easy way to achieve the above process:

1. First find out MIN
2. Next find out MAX

Then Find out total SUM .

TOTAL SUM - MIN  and TOTAL SUM - MAX , gives out the desired output,

As, 
if INPUT VALUES = 1,2,3,4,5

We are finding Actually:
1 . [1+2+3+4+5] -1(MIN)
1.  [1+2+3+4+5] -5(MAX) 

IN OTHER WORDS From Total, Take out Min
IN OTHER WORDS From Total, Take out Max

 which is shown in below:

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



CODE BY CODE BREAK
--------------------------

If input is 1 2 3 4 5
long min = arr.get(0) = 1;
long max = arr.get(0) = 1;
long sum = 0;
arr.size() = 5

for int i=0:
    arr.get(0)=1 < 1 [False]
    arr.get(0)=1 > 1 [False]
    sum = 0 + arr.get(0)=1 = 0+1 = 1
    
for int =1:
    arr.get(1)=2 < 1 [False]
    arr.get(1)=2 > 1 [True]
          max = 2
    sum = 1 + arr.get(1)=2 = 1+2 = 3

for int =2:
    arr.get(2)=3 < 1 [False]
    arr.get(2)=3 > 2 [True]
          max = 3
    sum = 3 + arr.get(2)=3 = 3+3 = 6
    
for int =3:
    arr.get(3)=4 < 1 [False]
    arr.get(3)=4 > 3 [False]
      max = 4
    sum = 6 + arr.get(3)=4 = 6+4 = 10
    
for int =5:
    arr.get(4)=5 < 1 [False]
    arr.get(4)=5 > 4 [False]
      max = 5
    sum = 10 + arr.get(4)=5 = 10+5 = 15

Hence Sum = 15

Max= 5
Min = 1

15-5 = 10
15-1 = 14

Hence it will return 10 and 14

  
```
</h3>
