# Part 1 - Debugging Scenario
<img width="504" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/6ac6b453-d4e4-4df3-8c47-04cb6b287048">


The code for the `ListExamples.java` is:

<img width="456" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/9aab4218-5357-4f11-ac51-72d2f6938da5">


The bug/symptom it showed was:

<img width="575" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/94a27815-3af0-4601-8838-32804428a3fc">


## TA Response:

Based on the output that you showed, you were expecting to run tests, however; it fails as the array lengths were different. This means
that there is something in your code that is affecting the size of the array. By looking at your code, I could see that on *line 26*,
your `index1` and `index2` have different lengths. Since you are trying to index it through the conditional loops, it is wise to start 
your index on **0** or in other words, you should change `index1` from **1000** to **0**. 

## Student Response:
<img width="390" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/3763cf68-6326-4d89-b0a6-b9490081a735">



<img width="577" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/5ddff49f-835a-4d0a-870f-be08608e26b1">


I did what you suggested and it worked!! You were right about the `index1` length, because I have started with **1000**, it affected the
rest of the code as the conditional statements only ran due to `index1` being smaller than `list1`. I fixed this bug by first typing
`nano ListExamples.java` on my terminal so I can access the code itself and replace the **1000** on `index1` with **0**. Then I saved
and exit, compile and ran tests by using `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and 
`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`. 

## Information needed for the setup
The file and directory I used was *ListExamples.java* in *lab7*. The contents before of *ListExamples.java* were:

<img width="477" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/366dfd63-d12a-4294-b340-94cf00690f14">


The full command lines I did to trigger the bug was `cd lab7` to enter the directory, `nano ListExamples.java` to access the code file
through the terminal, and then changing the size of `index1` to a very large number so that it will fail the `while` loops. To fix the 
bug, you can simply go back to the `ListExamples` file either through the terminal, which I used, or just clicking the file on the left 
primary side bar on *VScode*, and change `index1` size back to **0**.




# Part 2 - Reflection 
Something I learn that was pretty helpful on the second half of the quarter was being able to utillize the keyboard
shortcuts, which were so much efficient. For example, if I wanted to delete just one word from the previous text, 
rather than hitting the `backspace` button multiple times, I can just hit `Ctrl-W` which would delete the entire word. 
Thus, saving more time. Not to mention, `Ctrl-A` allows you to go all the way back to beginning of the line, which 
saves a lot of time than hitting the `arrow` key. 
