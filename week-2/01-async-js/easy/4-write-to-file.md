## Write to a file
Using the fs library again, try to write to the contents of a file.
You can use the fs library to as a black box, the goal is to understand async tasks.

// code to write and read contents of a file and print it to the console

const fs = require("fs");

fs.writeFile("a.txt", "I am a Sophomore", function(err, data)  {
  console.log("File written successfully.");

  fs.readFile("a.txt", "utf-8", function(err, data) {
    console.log(data);
  });
});