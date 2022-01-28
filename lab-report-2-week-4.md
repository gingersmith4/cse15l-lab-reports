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
![code change](error1.png)

Test file:

[link for test file](add the link)
![file](change1file.png)

Symptom of failure inducing output:
![error message](change1errorMessage.png)

Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.

### Change 3

Code change:
![code change](error1.png)

Test file:

[link for test file](add the link)
![file](change1file.png)

Symptom of failure inducing output:
![error message](change1errorMessage.png)

Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.

[Back to home page](index.html)