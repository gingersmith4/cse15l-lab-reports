# Lab report 2

Pick three code changes that your group worked on in labs 3 and 4 in order to fix a bug; these should be stored as commits on someone’s repository.
Fork the repository so you have your own copy with all the work your group did if you haven’t already.

For each of the three code changes:
Show a screenshot of the code change diff from Github (a page like this)
Link to the test file for a failure-inducing input that prompted you to make that change
Show the symptom of that failure-inducing input by showing the output of running the file at the command line for the version where it was failing 
(this should also be in the commit message history)
Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.

### Change 1

Code change:
![code change](error1.png)

Test file:

[link for test file](https://github.com/gingersmith4/markdown-parse/blob/main/test-three.md)
![file](change1file.png)

Symptom of failure inducing output:
![error message](change1errorMessage.png)

Here the bug was an assumption that the program could always subtract one from the index of the OpenBracket, the symptom was helpful because it showed that the program was looking at index 0 and -1 so we knew to look for a subtraction. The failure-inducing input is pretty rare, just if the very first thing in the file is a link. It took awhile to find the bug since the currentIndex starts at 0.

### Change 2

Code change:
![code change](change2edits.png)

Test file:

[link for test file](second-test.md)
![file](change2file.png)

Symptom of failure inducing output:
![error message](change2terminal.png)

Here the issue was that links without parentheses weren't being printed. Depending on the instructions for the program this could be a bug or we would want the "failure" because the link was not formatted correctly.

### Change 3

Code change:
![code change](change3edits.png)

Test file:

[link for test file](https://github.com/gingersmith4/markdown-parse/blob/main/test-four.md)
![file](change3file.png)

Symptom of failure inducing output:
![error message](change3terminal.png)

In this case the symptom was very clear from the failure-inducing input, there were quotes around the link in the test file. Then it was simple to fix the bug by checking if the link started with and ended with quotes and if so shifting the index over.


