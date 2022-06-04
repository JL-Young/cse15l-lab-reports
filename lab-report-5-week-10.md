# Lab Report 5 - Week 10

[JL-Young](https://github.com/JL-Young)

Return to [index](https://jl-young.github.io/cse15l-lab-reports/)

---
## Explain:
__How you found the tests with different results (Did you use vimdiff on the results of running a bash for loop? Did you search through manually? Did you use some other programmatic idea?)__

- I used _vimdiff_ to find the tests with different results. First, I added an echo at line 3 in the _script.sh_ file to print out the test names alongside their outputs. Then, I created a second script, _script2.sh_, to run all the tests with my implementation of MarkdownParse. Then, I recorded the outputs of the two scripts to two .txt files. Lastly, I used vimdiff to display the two files with their differences highlighted.

```
bash script.sh > results.txt

bash script2.sh > results2.txt

vimdiff <filename 1> <filename 2>

```

![vimdiff](lab-report-5/vimdiff.jpg)

__Provide a link to the test-file with different-results (in the provided repository or your repository , either is fine)__

- [test 41 page](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/41.html.test)

- [test 41 download](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/41.md)

- [test 512 page](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/512.html.test)

- [test 512 download](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/512.md)

---
## For each test:

1. __Describe which implementation is correct, or neither if both give the wrong output__

2. __Indicate both actual outputs (provide screenshots) and also what the expected output is (list the links that are expected in the output).__

3. __Decide on what it should produce (i.e., expected output) by using either VScode preview or the CommonMark demo site.__

4. __For the implementation that’s not correct (or choose one if both are incorrect), describe the bug (the problem in the code) in about 2-3 sentences. You don’t have to provide a fix, but you should be specific about what is wrong with the program, and show the code that should be fixed (Provide a screenshot of code and highlight where the change needs to be made).__

---
### Test 41

Mine is incorrect

![](lab-report-5/output-41.jpg)


![](lab-report-5/expect-41.jpg)

---

### Test 512

![](lab-report-5/output-512.jpg)

![](lab-report-5/expect-512.jpg)