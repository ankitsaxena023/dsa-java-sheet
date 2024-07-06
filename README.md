
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
