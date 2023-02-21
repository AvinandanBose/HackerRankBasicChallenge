<h3 align="Left">

```
Alice and Bob each created one problem for HackerRank. 
A reviewer rates the two challenges, 
awarding points on a scale from 1 to 100 for three categories: 
  problem clarity, originality, and difficulty.

The rating for Alice's challenge is the triplet a = (a[0], a[1], a[2]), 
  and the rating for Bob's challenge is the triplet b = (b[0], b[1], b[2]).

The task is to find their comparison points by comparing a[0] with b[0], 
  a[1] with b[1], and a[2] with b[2].

→If a[i] > b[i], then Alice is awarded 1 point.
→If a[i] < b[i], then Bob is awarded 1 point.
→If a[i] = b[i], then neither person receives a point.

Comparison points is the total points a person earned.

Given a and b, determine their respective comparison points.

------------------
Example
------------------
a = [1, 2, 3]
b = [3, 2, 1]

For elements *0*, Bob is awarded a point because a[0] .
For the equal elements a[1] and b[1], no points are earned.
Finally, for elements 2, a[2] > b[2] so Alice receives a point.
The return array is [1, 1] with Alice's score first and Bob's second.

------------------------------------
Function Description
----------------------------------

Complete the function compareTriplets in the editor below.

compareTriplets has the following parameter(s):

→int a[3]: Alice's challenge rating
→int b[3]: Bob's challenge rating

--------------------
Return
-------------
int[2]: Alice's score is in the first position, and Bob's score is in the second.
Input Format

The first line contains 3 space-separated integers, a[0], a[1], 
  and a[2], the respective values in triplet a.
  
The second line contains 3 space-separated integers, b[0], b[1], 
  and b[2], the respective values in triplet b.

Constraints
---------------------
1 ≤ a[i] ≤ 100
1 ≤ b[i] ≤ 100


Sample Input 0
-----------------------
5 6 7
3 6 10

Sample Output 0
-----------------------
1 1

Explanation 0
----------------------
  In this example:
  → a = (a[0],a[1],a[2]) = (5,6,7)
  → b = (b[0],b[1],b[2]) = (3,6,10)
  
  Now, let's compare each individual score:
  1. a[0]>b[0],So Alice recieves 1 point.
  2. a[1]=b[1], so nobody receives a point.
  3. a[2]<b[2], so Bob receives 1 point.
                
 Alice's comparison score is 1 , and Bob's comparison score is 1. Thus, we return the array [1,1].
  
 Sample Input 1
 --------------------
 17 28 30
 99 16 8
                
 Sample Output 1
 -----------------------
 2 1
                
 Explanation 1
---------------------
Comparing the 0th elements, 17<99 so Bob receives a point.
Comparing the 1st and 2nd elements, 28>16 and 30>8 so Alice receives two points.
The return array is [2,1] .             

```

</h3>
  
  
 <h3 align="Left">

```
Solution:
   
Approach : Its very simple that is we have to take two Array /List 
   and check compare their every elements through its index.
   
 Comparison given:
1. a[i]>b[i], 1 point.
  2. a[i]=b[i], so nobody receives a point.
  3. a[i]<b[i], so Bob receives 1 point.
Where , i = 0,1,2,3......

As the equal elements = no points recieved , hence we skip.
Scoring = Incrementing the values of variable, then we can add it to the List. 
                
So, basic approach of the problem will be:
 
  public static List<Integer> compareTriplets(List<Integer> a, List<Integer> b) {
    List<Integer> result = new ArrayList<>();
        int alice = 0;
        int bob = 0;
        for (int i = 0; i < a.size(); i++) {
            if (a.get(i) > b.get(i)) 
            {
                alice++; 
            } 
            else if (a.get(i) < b.get(i)) {
                bob++;
            }
        }
        result.add(alice);
        result.add(bob);
        return result;

    }

}
                                         
Other Approaches:
                                         
1) Using Iterable

 public static List<Integer> compareTriplets(List<Integer> a, List<Integer> b) {
        List<Integer> result = new ArrayList<>();
        Iterable<Integer> iterable = a;
        int aScore = 0;
        int bScore = 0;
        for (Integer integer : iterable) {
            if (a.get(a.indexOf(integer)) > b.get(a.indexOf(integer))) {
                aScore++;
            } else if (a.get(a.indexOf(integer)) < b.get(a.indexOf(integer))) {
                bScore++;
            }
        }
        result.add(aScore);
        result.add(bScore);
        return result;

    }

}

                                                                             
2) Using Iterator
                                                                             
 public static List<Integer> compareTriplets(List<Integer> a, List<Integer> b) {
        List<Integer> result = new ArrayList<>();
        Iterator<Integer> aIterator = a.iterator();
         Iterator<Integer> bIterator = b.iterator();
        int aScore = 0;
        int bScore = 0;
        
        while(aIterator.hasNext() && bIterator.hasNext()) {
            int aVal = aIterator.next();
            int bVal = bIterator.next();
            if(aVal > bVal) {
                aScore++;
            } else if (aVal < bVal) {
                bScore++;
            }
        }
        result.add(aScore);
        result.add(bScore);
        return result;

    }

}                                                                           

   

```

</h3>
