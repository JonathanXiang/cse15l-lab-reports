# Lab Report 4
By Jonathan Xiang

## Step 4 - Logging into ieng6

![](Step4LogIn.png)

*Keys Pressed:* ssh cs15lwi23aoy@ieng6.ucsd.edu`<enter>`

Because I previously generated an ssh key on the computer I'm using, I didn't have to type in the password to log in.

## Step 5 - Cloning the Forked Repository

![](Step5Fork.png)

*Keys Pressed:* git clone git@github.com:JonathanXiang/lab7.git`<enter>`

Since I had generated an ssh key for my github before, I was able to use the repository's ssh link instead of its https link to clone it.

## Step 6 - Running the Test

![](Step6Test.png)

*Keys Pressed:* cd lab7`<enter><ctrl + v><enter>`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`<enter>`

Before doing the tasks, I copied `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` to my clipboard, allowing me to use `ctrl + v` to quickly paste the command down.

## Step 7 - Fixing the Test

![](Step7Nano.png)

*Keys Pressed:* nano ListExamples.java`<enter><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><right><right><right><right><right><right><right><right><right><right><right><right><backspace>`2`<ctrl + o><enter><ctrl + x>`

I opened ListExamples.java in nano and then used the arrow keys to navigate to where I needed to edit the file, changing an `index1` to an `index2`.

## Step 8 - Rerunning the Test

![](Step8TestRerun)
