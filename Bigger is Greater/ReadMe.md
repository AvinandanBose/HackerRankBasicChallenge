![Screenshot (264)](https://user-images.githubusercontent.com/38869235/221263279-0599e517-4f6c-4f3b-acd8-4f83c5081b65.png)
![Screenshot (265)](https://user-images.githubusercontent.com/38869235/221263315-d69fc365-800c-4c39-83f7-2e0c75ebd0b8.png)
![Screenshot (266)](https://user-images.githubusercontent.com/38869235/221263323-cc0b6990-aea1-44ce-b4ee-bd35d1681e9b.png)
![Screenshot (267)](https://user-images.githubusercontent.com/38869235/221263340-998fca3f-2d19-43b2-b091-e17c8c3282e7.png)
![Screenshot (268)](https://user-images.githubusercontent.com/38869235/221263663-4cfca977-bc74-46c1-a1c4-6e9ffb0b4faf.png)
![Screenshot (269)](https://user-images.githubusercontent.com/38869235/221263681-067257b7-aad8-4f7b-a6ec-e2e5f04303cb.png)
![Screenshot (270)](https://user-images.githubusercontent.com/38869235/221263686-bc60cca0-634e-4be0-8e3c-7b2d4a7e3c9f.png)


<h3 = "Left">


```
Solution:

 public static String biggerIsGreater(String w) {
    char[] chars = w.toCharArray();
        int i = chars.length - 1;
        while (i > 0 && chars[i - 1] >= chars[i]) {
            i--;
        }
        if (i <= 0) {
            return "no answer";
        }
        int j = chars.length - 1;
        while (chars[j] <= chars[i - 1]) {
            j--;
        }
        char temp = chars[i - 1];
        chars[i - 1] = chars[j];
        chars[j] = temp;
        j = chars.length - 1;
        while (i < j) {
            temp = chars[i];
            chars[i] = chars[j];
            chars[j] = temp;
            i++;
            j--;
        }
        return new String(chars);

    }

}

```
</h3>
