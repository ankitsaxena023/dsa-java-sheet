
# Dsa-Java+JS-Sheet
```
Emphasis and Lists:
Use *italic* or **bold** to add emphasis.
Create bulleted or numbered lists.

Headers:
Use #, ##, ###, etc., for different levels of headings.

Links:
Create hyperlinks using [link text](URL).

Images:
Embed images with ![alt text](image URL).

Code Blocks:
Present code using triple backticks (`) to create code blocks. You can specify the programming language for syntax highlighting after the first triple backtick, like ```python.

Tables:
Design tables using the | symbol to separate columns.

Horizontal Lines:
Add horizontal lines with three hyphens (---) or asterisks (***).

Blockquotes:
Use > to create blockquotes for important information or quotes.

Inline Code:
Highlight inline code with backticks, like inline code.

Footnotes:
Include footnotes using [^1] and define them at the bottom of your document.

Math Formulas:
If your project involves mathematical expressions, you can use LaTeX-style math notation enclosed in $$ for block-level math, or $ for inline math.

Checkboxes:
Create checkboxes by using - [ ] for an unchecked box and - [x] for a checked box.

Task Lists:
Use - [ ] to create task lists, which can be used for tracking to-dos or milestones.

GitHub Flavored Markdown (GFM):
GitHub supports some additional features such as @mentions, issue and pull request linking, and automatic linking of URLs.

Emoji:
You can use emoji in your README to add some personality and context. For example, :smile: or :rocket:.

```
---
## Capitalize the first char of each word of a String (JS)
```
const str = "sHoRt AnD sToUt";
const a1 = str.toLowerCase().split(" ");
for(let i=0; i<a1.length ; i++){
  a1[i]= a1[i].charAt(0).toUpperCase() + a1[i].slice(1);
}
  console.log("charIndex", a1.join(" "))
```

---
## Reverse a string (Java)

### Notes : for initialize character we use '\0', eg:  char ch = '\0';

```
import java.util.*;

public class Main {
    public static void main(String[] args) {
      String str = "Hello";
      
      String str2 = "";
      char ch = '\0';
      
      for(int i=0; i<str.length(); i++){
        ch = str.charAt(i);
        str2 = ch + str2;
      }
      System.out.print(str2);
  }
}
```
---

## Pelindrome a string (Java)
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
      String str = "racecar";
      
      // String str2 = "";
      // char ch = '\0';
      
      // for(int i=0; i<str.length(); i++){
      //   ch = str.charAt(i);
      //   str2 = ch + str2;
      // }
      
      // if(str.equals(str2)){
      //   System.out.print("It's a palindrome");
      // }else{
      //   System.out.print("It's not a palindrome");
      // }
      
      int left = 0;
      int right = str.length() - 1;
      
      while(left <= right){
        if(str.charAt(left) != str.charAt(right)){
          System.out.println("It's not a palindrom");
          return;
        }
          left++;
          right--;
      }
      System.out.print("It's a palindrom");
  }
}
```


---
## Array Intersection
```
function arrayIntersection(arr1, arr2) {
  const set1 = new Set(arr1);
  const intersection = [];

  for (let num of arr2) {
    if (set1.has(num)) {
      intersection.push(num);
    }
  }

  return intersection;
}

console.log(arrayIntersection([1, 2, 3, 4, 5], [3, 4, 5, 6, 7]))
```
```
function arrayIntersection(arr1, arr2) {
  let arr3 = [];
  for(let i=0; i<arr1.length; i++){
    if(arr2.includes(arr1[i])){
      arr3.push(arr1[i]);
    }
  }
  return arr3;
}
```

---
## Remove Duplicate
```
function removeDuplicates(arr) {
  for(let i=0; i<arr.length; i++) {
    //! Solution 1 -
    // const arraySet = new Set(arr);
    // return Array.from(arraySet) ;

    //! Solution 2 -
    const uniqueArr = [];

    for(let i=0; i<arr.length; i++) {
      if(!uniqueArr.includes(arr[i])){
        uniqueArr.push(arr[i]);
      }
    }
    return uniqueArr;
  }
}

const result = removeDuplicates([
  1,
  2,
  3,
  4,
  5,
  5,
  5,
  6,
  7,
  8,
  'hello',
  'hello',
  true,
  true,
]);

console.log(result);
```

---
## FizzBuzz Array

### In this challenge, you will write a function called `fizzBuzzArray` that takes in a number and returns an array. The array should contain all the numbers from 1 to the number passed in. However, if the number is divisible by 3, you should replace the number with "Fizz". If the number is divisible by 5, you should replace the number with "Buzz". If the number is divisible by both 3 and 5, you should replace the number with "FizzBuzz".

```
function fizzBuzzArray(num) {
  const array = [];

  for (let i = 1; i <= num; i++) {
    if (i % 3 == 0 && i % 5 == 0) {
      array.push("FizzBuzz");
    } else if (i % 5 == 0) {
      array.push("Buzz");
    } else if (i % 3 == 0) {
      array.push("Fizz");
    } else {
      array.push(i);
    }
  }
  return array;
}

const result = fizzBuzzArray(15);

console.log(result);

```
---
## Find target element in sorted array
```
import java.util.*;

public class Main {
    public static int binarySearch(int arr[], int target){
      int left = 0;
      int right = arr.length - 1;
      
      
      while(left <= right){
        int mid = left  + (right - left)/ 2;
    
        if(arr[mid] == target){
          return mid;
        }else if(arr[mid] < target){
          left = mid + 1;
        }else{
          right = mid - 1;
        }
      }
      return -1;
    }  
  
    public static void main(String[] args) {
      int arr [] = {2,5,8,12,16,23,38,56};
      int target = 38;
      
      int result = binarySearch(arr, target);
      System.out.println("result "+result);
      
      if(result != -1){
        System.out.println("target is present in index "+result);
      }else{
        System.out.println("target is not present in the array");
      }
      
  }
}
```
