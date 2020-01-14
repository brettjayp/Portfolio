# 201n15-lab-02
Code Fellows, Class 201n15, Lab 02

README - Brett Packard, Class 201n15, Lab 02, ABOUT ME

The objective of this lab, at this time, is to create an "About Me" webpage that has a "game" that meets certain grading criteria, using the knowledge we've learned so far and are capable of.

Some of the requirements that I think are key to focus on are as follows:
-At least 5 questions.
-Questions must be a mix of yes/no and user input questions.
-All yes/no questions must accept yes, no, y, and n, with any combination of type case.
-Need to create useful and descriptive output into console.log
-Must remember to follow ACP frequently.

Some initial brainstorming brings me to an idea, "Are we friends?", where the webpage asks a series of questions regarding the user's interests and personality traits, and in the end, it will tell the user if it thinks they would be friends with me. I think that the easiest way to do this at this point in my education is to ask several y/n questions such as "do you like X activity?" and find a way to tally the yes answers, and if they exceed a threshold, give a positive result to the user. It would be difficult at this time to factor complex answers, such as "what is your favorite TV show?", but those could be an excellent way to include details about the user in the final output, ie "I would love to watch 'fav tv show' with you", regardless if the outcome is positive or negative. While the interactions in the game revolve around the USER'S input, it would tie in to an "About Me" project because it would compare "About Me" with "About you", and I could creatively tie in comparisons to "About Me" in the final page output.

I've now created my main variables, and prompt questions for them. I'll probably need to refine them later, and I definetly want to make them a bit more interactive. I think what I'll need to do now in order to be able to tally all the "yes" responses is to create a second set of variables, in parallel to the main answers, and set their values to either 0 or 1, 1 if the original is a yes. A very roundabout way, not efficient whatsoever, but it's what I have available to me at this time in the class. At the end, there will be a final value variable ("answerTally" or something like that), and if it's equal to or greater than 7 (total possible is 10), then the user gets the positive result as an output.

I took the time to convert all the answers to binary values, only to remember I didn't need to. Attention to detail! Correction to the statement in the previous paragraph, there are a total of 7 yes/no questions, so I'll set the threshold to qualify as a friend as 5/7. Will go back and remove the code to convert the non-yes/no answers to binary values.

August 17, 19 (pair programming with James)
I worked on js and created a function to run yes/no questions, and to score 1 point everytime the user chooses the right answer. And at the end it makes a sum of all points and displays a fancy message according to the obtained score! This saved 70 lines of code. 

August 20, 2019
Continued to work on js.app . Added functions to make all questions after the first question "react" to the previous yes/no question's result, or in the case they follow a question other than yes/no, they still "react" but without discrimination. Also changed choice of color palette to use for styling.

August 21, 2019
-I've completed converting all of the questions in my About Me game into their function form. It's a substantial amount of text, but it all works out well! I've also decided to set the game to only run when the user clicks a button to initiate the game. I think either Leo or Noah did that(?) and I liked that, since I personally wouldn't want to be forced to have 14 uninvited alerts and prompts EVERY time I reload the page. I'm pretty late on getting this page to where it should be, so let's start making it look like an actual webpage!
-Given that my entire app.js is now basically one function that spans 107 lines, I think that I want to dedicate a single .js file to just that game function now. I'm not going to do that RIGHT now, but I plan to do so.
-I've added an attractive nav bar to the top of my page, in a fixed position to keep it always present, utilizing a gradient of some of my palettle colors.
-Added a directory for photo library. Currently contains one photo, an edited stock photo.

August 25, 2019
-Really getting to this all so late, I'm really far behind. I've been super busy and got sick. Anyways, see below for a summary of my most recent changes.
-I've completed my general parallax scrolling effect. I pulled some good looking images of wood and shingles for backgrounds, this gives a common theme between them that isn't distracting. I've found that it does make it hard to read text over them, so I added a 0.5 opacity black bar behind the text over the images, and added a white shadow to the text to further increase contrast.
-I've reworked the "About Me" game in order to assign the user's answers to global variables. This is very important, because I plan to display their answers in the page. I might later decide I want to save all of the answers, output to a persistent log, to keep a record of. There's plenty I could do with that.
-Completed the two remaining lab-03 questions. Implemented as buttons, as I don't feel like integrating them into the overall score tally system at this time, due to turning in so late.

August 26, 2019
-Time to wrap up the page. I have my parallax scroll effect working, I have all my game functions working (even if I have some of them separated at the moment), and I have my layout that I plan to use. I need to populate my page's sections with information, styling to organize it within those sections, and to put together the display I had in mind to present the results when the user plays my game.
-I'll start by populating information into my sections. Links, details, information. Then I'll style it, I'm thinking of 0.5 opacity white boxes, with text over in a color from the color palette chosen.

August 27, 2019
-Wow. This whole time I've been running my linux environment as a VM on my Windows machine, running it exactly as the pre-work described. That was proving troublesome. So I've spent some time to migrate from a VM to a dual boot solution, freeing up my system's resources and cutting out bugs. The first time that I finally opened my webpage after getting set up, my webpage looks like CRAP!!! First off, no photos. Dummy me, I was referencing all my photos by their absolute paths, rather than their relative paths. Second off, everything was oversized. Again, dummy me, I was not running the VM in it's native resolution, I was stretching it to fit. As a result, running my page on a system running properly, I notice that everyting I saw was not running at the proper resolution, and appeared different than it would on another system.
-First, I need to fix this. Fortunately, this should be really easy. Running my page at 50% makes it look perfect! So I'll start by halving every size I've set. Second, lessons learned!

August 29, 2019
-I've been fighting to get DIV's side by side. I should know how by now. I found a neat way doing so while looking online (using flex and flex-grow), but what I take from it is more fundamental, and that's that I need to be mindful of trying to fit one thing in another. If I had tried creating a container DIV for these boxes in the first place, I don't think I would have struggled so much.

August 30, 2019
-Cleaned up a few lines of unnecessary code in css and html. Adding more content to html page. Improved styling a little bit. Added a link to a google image search for dogs (I know, I now have an almost perfect website now, you're welcome, woof). Decluttered some things in the html page. Fixed linter callouts. Almost ready to submit for lab 5b.
-Still need to: __Ensure 1 or 2 checkmarks for text contrast via Chrome (stretch). __Create and save an SSH key for working with GitHub. __I need to (eventually) find a list that actually works for using an ordered list, currently I just made one an ordered list for the sake of having at least one. __Have answers for my main guessing game go into an array, though I do use an array already for my last guessing game. __Audit my site for accessability. __Deploy my page on GitHub, this is what I'm doing next.
-About to deploy on GitHub.

September 02, 2019
-Having now watched class 6, getting more comfortable with object literals, I decided to re-write my "About Me" game. It looks a ton better, and I think I'm definitely more comfortable working with arrays and object literals. I also had to re-write the button to display the results. The console.log output from that button looks great!