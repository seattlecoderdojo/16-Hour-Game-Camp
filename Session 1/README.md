# Session 1 Student Guide: Shall We Play A Game?

[Looking for the instructor's notes?](InstructorNotes.md)

## Let's get signed up

The first step here is to get signed up with [PlayCanvas](https://playcanvas.com). You'll need an email address and you'll need to pick a password. If you have a GMail account that isn't a school account, you can use that to login.

PlayCanvas will provide all the software tools we'll need for this course in the browser.

## Once you're signed up and logged in...

The top of the screen will have a tab titled "Explore." Click it and you can explore a number of games created with PlayCanvas. The one we're going to try is called "[Keepy Up.](https://playcanv.as/p/XtfZXpxU/)"

[![Keepy Up Title Screen](../Resources%20and%20Assets/tutorial_images/keepy_up_open_screen_1.jpg)](https://playcanv.as/p/XtfZXpxU/) 

Try and play it. You'll get a few minutes. Think about what makes it fun or hard (or boring). 

The instructor's going to talk with you about the game play (if you're doing this on your own read [the instructor's notes](InstructorNotes.md)). If you aspire to develop games, the coding is just the way you turn your (or your team's) concept into something that can actually be played. So we'll pause now and again to think about what makes a good game good.

## Your First Project

Here we're going to switch to PlayCanvas' [your first app tutorial](https://developer.playcanvas.com/en/user-manual/your-first-app/).

## Your Second Project

With a few minutes left, we'll do a quick number guessing game to explore the coding concepts we learned.

Let's go to [repl.it](https://replit.com/), which will give us a quickie coding environment for an easy JavaScript text game. Create an account or login with your GMail account. Once you're signed in, select "My repls" in the lefthand navigation links. Then click the "+ New repl"

![new repl](../Resources%20and%20Assets/tutorial_images/newRepl.jpg)

You can create a programming environment for a bunch of different languages, but we'll use Node.js. It will assign you a name like the one shown above, or you can make one up. Create the repl.

We'll need to add a package that makes it easy to get a response from the player. In the icons on the side, go to the one that looks like a cube and says"packages" when you put your mouse over it. Click it.

![packages](../Resources%20and%20Assets/tutorial_images/packages.jpg)

Search for a package called `prompt-sync`. When it comes up, click it, then click the "Add" button.

Now in the "index.js" file, paste this code.

```javascript
// This is some basic code we're using to set up some structure
const prompt = require('prompt-sync')();

// this is where our code starts
var winner = false; // is the player a winner yet?
var lower = 1; // our lower bound
var upper = 50; // our upper bound
var num = Math.floor(Math.random() * (upper - lower)) + lower; // generate our number
var question = `Pick a number between ${lower} and ${upper}: `;
var baseq = question;

// this is a "while loop" it will keep running 
// until the variable winner is something other than true
while (winner == false) {
  let guess = prompt(question);
  console.log(guess);
  winner = true;
}

console.log("done");
```

We can break this down... up at the top, we use const to set up a variable named prompt. Using the const keyword tells JavaScript we're only ever going to set the contents of this variable once. If we try to set it again, it should fail.

Now we set other values. `winner` is false because the game is just starting. Our randomizer will pick a number between lower and upper. `num` sets the random number using `Math` functions. Then we set our `question` AND make a copy of it in `baseq`.

We're using three types of variables here. The types are defined by what they contain.

- `winner` is a Boolean value. Booleans are true or false.
- `upper`, `lower`, and `num` are integers. Integers are whole numbers with no decimal point like 2 and 564.
- `question` and `baseq` are strings. Strings contain text like words and sentences. When you define text you put quotes ('), double-quotes ("), or backticks (`) on both sides of the text.
  - With backticks, you get a "template string" that allows you to include other variables inside it using `${variable_name}`.

