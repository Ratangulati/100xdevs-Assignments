## File cleaner
Read a file, remove all the extra spaces and write it back to the same file.

For example, if the file input was
```
hello     world    my    name   is       raman
```

After the program runs, the output should be

```
hello world my name is raman
```

// Solution 
const fs = require('fs');

fs .readFile("a.txt", "utf-8", (err, data) => {
  console.log(data);
  
  let updatedData = data.replaceAll(/\s+/g, " ");
  console.log(updatedData);
});


// \s: matches any whitespace symbol: spaces, tabs, and line breaks
// +: match one or more of the preceding tokens (referencing \s)
// g: the g at the end indicates iterative searching throughout the full string