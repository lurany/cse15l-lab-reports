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




# Part 2 - Reflection 
Something I learn that was pretty helpful on the second half of the quarter was being able to utillize the keyboard
shortcuts, which were so much efficient. For example, if I wanted to delete just one word from the previous text, 
rather than hitting the `backspace` button multiple times, I can just hit `Ctrl-W` which would delete the entire word. 
Thus, saving more time. Not to mention, `Ctrl-A` allows you to go all the way back to beginning of the line, which 
saves a lot of time than hitting the `arrow` key. 
