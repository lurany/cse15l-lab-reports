# Lab Report 4
## Step 4 - Log into ieng6
<img width="385" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/c87090d8-1233-4f95-aca7-313377d6ba07">

To log into my ieng6 account, I simply just typed:

`$ ssh cs15lsp23xx@ieng6.ucsd.edu <enter>`

in the terminal since `<enter>` allows the terminal to run the command.
Since I have already set up a **SSH key**, I am able to log into my
remote account without the need to type my password in.
## Step 5 - Clone your fork of the repository from your Github account
<img width="306" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/d6af8be5-4a71-41ad-942f-cbebc5d0a429">

<img width="416" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/41ae03e1-20e7-4197-8759-2479e176aa89">

As we can see, I have already link my GitHub to my remote account during my lab, so all I need to do right now is to use ssh on GitHub
to clone it into my ieng6 account. I typed:

`$ git clone <link from GitHub> <enter>` 

and it should be able to clone. However, I have already cloned it earlier so my lab7 already exits and the directory is no longer empty,
which is why it shows up like that. 
## Step 6 - Run the tests, demonstrating that they fail
<img width="422" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/bea6afe3-afdf-48a6-a8c8-cb9efd24dc51">


During this step, we expect the tests to fail, but first we would need to compile the files in the directory. First, in order for me
to get into the right directory, I typed:

`$ cd la<tab>` 

which would basically bring me to *lab7* directory. I used `<tab>` because tab basically autofil the directory as long as there aren't
any files with similar names in the root directory. Next, I typed `<Ctrl-C> javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` 
to copy the command and `<Ctrl-V> javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>` to paste the command into my terminal
in order to compile the files. Afterwards, I did the same thing `<Ctrl-C> java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` to copy and `<Ctrl-V> java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests <enter>` to paste the
command to run tests on the terminal. 

## Step 7 - Edit the code file to fix the failing test
## Step 8 - Run the tests, demonstrating that they now succeed
## Step 9 - Commit and push the resulting change to your Github account 


