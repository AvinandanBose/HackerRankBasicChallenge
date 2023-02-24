![Screenshot (249)](https://user-images.githubusercontent.com/38869235/220712246-ad59a17b-4412-4605-939e-315b4a5efb31.png)
![Screenshot (250)](https://user-images.githubusercontent.com/38869235/220712409-61cd2202-4617-4fb1-98d9-53a56b551391.png)


<h3 align="Left">
  
```
  Solution:
  
  public static int birthdayCakeCandles(List<Integer> candles) {
    int max = 0;
        int count = 0;
        for (int i = 0; i < candles.size(); i++) {
            if (candles.get(i) > max) {
                max = candles.get(i);
                count = 1;
            } else if (candles.get(i) == max) {
                count++;
            }
        }
        return count;

    }

}

----------------------------------------------------
  Explanation: 
------------------------------------------------------------ 
  You are in charge of the cake for a child's birthday. 
You have decided the cake will have one candle for each year of their total age. 
They will only be able to blow out the tallest of the candles. 
Count how many candles are tallest. Eg : Candles =[4,4,1,3], The maximum candles are 4 units high . 
There are 2 of them , so return 2. 
Hence explanation is very easy that we would be given an array ,
where units of candles will be given and from there we have to count number higher units . 
	
	
		


So is the below program is doing:

public static int birthdayCakeCandles(List<Integer> candles) {
    int max = 0;
        int count = 0;
        for (int i = 0; i < candles.size(); i++) {
            if (candles.get(i) > max) {
                max = candles.get(i);
                count = 1;
            } else if (candles.get(i) == max) {
                count++;
            }
        }
        return count;

    }

}

Where , List<Integer> takes units of candles 
max and count is zero initially .  Lets take the above eg:  [4,4,1,3]

Now there is 2 condition :

1st Condition : when we get the max unit , we make the count = 1

2nd Condition: How many same max unit we get , we do count= count+1(count++).

Now, code by code breakdown
-------------------------------------
Candles.size() = Number of elements = 4
for int i =0

	if (candles.get(0)=4 > max=0): True

			max = candles.get(0)=4
			count = 1
Then:
int i =1	
	if (candles.get(1)=4 > max=4):False

	Else if: (candles.get(1) =4 == max =4):True
			count ++ = 1+1 = 2

Then:
int i =2
	if (candles.get(2)=1 > max=4):False

	Else if: (candles.get(2) =1 == max =4):False

int i =3
	if (candles.get(3)=3 > max=4):False

	Else if: (candles.get(3) =3 == max =4):False
			
Hence count = 2 (Ans)
=========================================================================
	
There is another approach:
	
public static int birthdayCakeCandles(List<Integer> candles) {

        int max = 0;
        for (int i = 0; i < candles.size(); i++) {
            if (candles.get(i) > max) {
                max = candles.get(i);
            }

        }

         Iterator<Integer> itr = candles.iterator();
        while (itr.hasNext()) {
            if (itr.next() < max) {
                itr.remove();
            }
        }
        return candles.size();
    }
}

Here we find out the max and in another we remove the elements and keep all max.
				 
Suppose we have [1, 14, 15 ,70,70]
max= 70
After remove all element candles have = [70,70]				
Hence Size = 2 [Expected Output],
But here we see Line of Code and Two iteration we use , hence Time Complexity also increases ,
Hence First approach is more optimized.

	
  
```
  
</h3>
