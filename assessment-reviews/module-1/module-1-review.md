# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for?

Html stands for hypertext markup language. It is responsible for the structure or layout of electronic documents and webpages such as headings, paragraphs, lists, etc. HTML is not considered a true programming language because it doesn't process or manipulate data. 

2. What is the difference between an ID and a class?

An ID typically only has one element assigned to it while a class typcially has several elements assigned to it. IDs and classes are used to apply styling using CSS to the elements.

3. What does it mean to write "semantic" HTML?

Semantic HTML is used to emphasize the meaning of the information on the webpage. 

### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!".

'''
<p class="highlight">Watch out!</p>
'''

2. Write an HTML image tag to show an image called `profile-picture.jpg`.

'''
<img src=`profile-picture.jpg`>
'''

3. Write a link tag that links to http://google.com.

'''
<a href="http://google.com">google</a>
'''

5. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).

'''
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="main.css">  
  </head>
  <body>
    <ol>
      <li>Sapiens</li>
      <li>Way of the Peaceful Warrior</li>
      <li>Anne of Green Gables</li>
    </ol>
    <script src="main.js"></script>
  </body>
</html>
'''

6. Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.
7. Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.
8. Write a numbered list in HTML and list three of your favorite books.
9. Fix the indentation of the following HTML sample:

  ```html
  <div>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
  </div>
  ```

## CSS

### Questions

1. What is CSS and what is it used for?

Cascading Style Sheets (CSS) is a language used to add style to webpages. It is used to determine color, font, size, border, spacing and location of HTML.

2. What is the CSS box model?

Wrapped around every html element is a box referred to as the CSS box model. The CSS box model consists of the margin, border, padding and content.

3. What's the difference between margin and padding?

Margin is the outermost box and clears the area from the border to the end of the webpage. Padding lays between the content and the border and determines how much space is between content and the border. Both margin and padding are transparent. 

### Exercises

1. Write a CSS rule to make the text of all `h1` tags red.

'''
h1 {
  color: red;
}
'''

2. Write a CSS rule to make the background color of the link with `class="btn"` blue:

  ```html
  <a href="#" class="btn" style="background-color: blue;">Learn more</a>
  ```

3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.

  ```html
  <header class="jumbotron">
    <p style="font-size: 20px;">Hello, World!</p>
  </header>

  <p>Welcome to this awesome website!</p>
  ```

## JavaScript

### Questions

1. What is a function? What are they used for?

Functions are a set of instructions (blocks of code) that perform a certain task/function/behavior. They are used to help keep code DRY.

2. What is the difference between `==` and `===`?

The == is equal to. The double equal sign == attempts to convert the type of the value on the left side to the same type as the value on the right side and then check if the comparison is true. The strict equality operator (===) denotes equal value and equal type. It tests to make sure that the code on either side of it evaluates to both the same value and type.

  "5" == 5 is true.
  "5" === 5 is false. 

3. What is the difference between global and local scope variables?

Variables can be defined inside or outside of functions. Local scope variables are defined inside a function are only available to that function. Global variables are defined outside of functions and are available for use in the entire script.

4. What is a boolean value?

A boolean is a data type that expresses whether code is true or false. Booleans must be written with all lowercase lettering.

5. What is an array?

An array is a type of JavaScript object that stores an indexed list of data.

### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.

```javascript
var myName = "Dawna";
```

2. Write a loop that logs the numbers 1 through 10 to the console.

```javascript
for (var i = 0; i > 10; i++) {
  console.log("Number " + i);
}
```

3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".

```javascript
var score = 7;
var lives = 2;

if (score > 3 && lives > 0) {
  alert("You Win!");
}
```

4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, 'name'!" to the console. Then, call the function below the function definition and pass in your name as the argument.

```javascript
var sayHello = function(name) {
  console.log("Hello, " + name + "!");
}

sayHello("Dawna");
```

5. What would the following script log to the console?

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  ```
Friday, Friday

6. What would the following script log to the console?

  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  10
  ```

7. What would the following script log to the console?

  ```javascript
  var helloGoodbye = function(name) {
    return sayHello(name) + " " + sayGoodbye(name);
  }

  var sayHello = function(name) {
    return "Hello " + name + "!";
  }

  var sayGoodbye = function(name) {
    return "Goodbye " + name + "!";
  }

  console.log(helloGoodbye("Sarah"));
  ```
  
  Hello Sarah! Goodbye Sarah!

8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.

```javascript
var findLongestWord = function(words) {
  var longestWordLength = 0;
  
  for (var i = 0; i < words.length; i++) {
    if (words[i].length > longestWordLength) {
      longestWordLength = words[i].length;
    }
  }
  
  return longestWordLength;
}
```

9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.

```javascript
var sum = function([a, b, c, d]) {
  return a + b + c + d;
}
```

10. Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.

```javascript
function character(string) {
  if (string === "a" || string === "e" || string === "i" || string === "o" || string === "u") {
    return true;
  } else {
    return false;
  }
}
```

11. Write the correct line to make `"Woof!"` show up in the console based on this script:

  ```javascript
  var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
    }
  };
  ```
pet.speak();

12. Using the same script as above, write the correct line to log the dog's name to the console.

console.log(pet.name);

## Command Line

### Questions

1. What is the command line and what is it used for?

The command line allows developers to navigate their filesystem, alter files, execute programs, install software, create new applications, and much more. We use the terms command line, command line prompt, terminal, and shell interchangeably in the developer community.

2. What does the command `ls` do?

The ls command will list the contents of directory that you are currently in.

3. What does the command `pwd` do?

pwd stands for print working dirctory and it prints the the name of the current directory to the command line. 

4. What does the following command do: `cd my-cool-project`

Switches or changes into the dirctory my-cool-project.

### Exercises

1. Write the command to make a new directory called "my-cool-project".

mkdir my-cool-project

2. Write the command to create a file called "index.html".

touch index.html

3. Write the command to delete a file called "main.css".

rm main.css

## Git

### Questions

1. What is Git and what is it used for?

Git is a version control system. It is used to track changes in a project and undo them if necessary. 

2. What's the difference between a local repository and a remote repository?

A local repository is a version that a person has on their computer. The remote repository is what is up on github. 

### Exercises

1. Write the command that you would use to create a new local Git repository.

git init .

2. Write the command to stage a file called `index.html` to be committed.

git add index.html

3. Write the command to view the current status of the git repository.

git status
