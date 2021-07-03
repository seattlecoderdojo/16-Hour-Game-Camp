# Session 1: Instructor's Notes

[Looking for the student guide?](README.md)

First and foremost, read the student guide. Most things are explained there. Here you'll find extra insights, troubleshooting tips, and other useful stuff.

## Steps in the lesson

* Get them signed up with Play Canvas (10 minutes)
  * Why 10 minutes? Because some kids won't remember their email address or their email password or will need some sort of help getting getting one... No matter what you tell them to prepare, some won't. 
    If you're a teacher, you know this from experience. 
    If you're a tech pro, jumping in to teach something fun, *everything* will take longer than you think. 
  
* Play a Demo Game (10 minutes)
  * They'll play "[Keepy Up](https://playcanv.as/p/XtfZXpxU/)." You try to keep the ball in the air. This is the game for their "[Making a Simple Game](https://developer.playcanvas.com/en/tutorials/keepyup-part-one/)" tutorial. Help them find it and let them play it.
  
* Discuss the Demo Game (10-15 minutes)
  * Ask them questions about how hard it was to figure out how to play?
  * Were there any surprises?
  * Did they like it? What did they like?
  * Talk about the physics of the game. While they're mostly taken care of by the game engine, the game utilized gravity and reflection (the ball bouncing off the point where you clicked it rather than straight up).
  * Talk about the "win condition" - In this game, the goal is just to keep the ball in the air. What are other variations they can think of? Possibly a timed version where you try to get the most bounces and the timing of the clicks changes the force of the bounce.
  * How could they increase the difficulty? Increase gravity so the bounces are lower and the ball falls faster? Add another ball? Make the ball smaller?
  
* Your first project (30 minutes)
  * We jump out to PlayCanvas' first tutorial... [Your First App](https://developer.playcanvas.com/en/user-manual/your-first-app/)
  * Walk them through the pre-coding steps.
  * At "Now hit EDIT to open the Code Editor. You'll see the following skeleton script:" stop and help the kids start understanding the code they're about to use.
  * The code will be too complex to go through entirely, but focus on three concepts:
    * 1: A function is a collection of code, sort of like a program within a program, that other code in the program can call on to do complex things. You generally use functions for something the code will do more than once. In this case, the update function they'll be editing is called by the main program to run for every frame of the animation.
      * If they don't understand frames, explain. If they've done any serious gaming they know FPS. Otherwise use TV and movies.
    * 2: var - a variable. For now just explain it as a bucket you put something in. Here the keyboard variable contains all the information known about the keyboard at the time. Then the left, right, up, and down variables are created to hold a true/false value... is this arrow key pressed?
    * 3: if - What we put in the parentheses should either be a true/false value or be able to be evaluated for a true/false. If the variable left has the value true, we move the entity (which is the ball). You could use an if to test if a variable has the value of 100... `if (b == 100)` will evaluate to true if b does equal 100. If b equals anything else, it'll be false.
  * Otherwise, just have them copy and paste it from the tutorial into their project. BE PREPARED FOR THEM OVERCOPYING, UNDERCOPYING, OR PASTING IN THE WRONG PLACE.
  * They have now created their first 3D app. It's not a game, but they're getting the hang of the editor. Let them mess around with their existing app or go back to the Keepy Up game and think about how what they learned might be getting used under the hood.
  * Give them a break to let their brains absorb
  
  ## break 10 minutes
  
  Last section... basic code, making a guessing game.
  * Let's go to [repl.it](https://replit.com/), Follow the instructions for creating a new repl. If the kids are curious what a repl is, it's an acronym for Read Evaluate Print Loop. But it's come to be a simple encapsulated programming environment that can run the code you wrote and can be embedded in a web page or a computer program.