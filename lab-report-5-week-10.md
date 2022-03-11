# Lab Report 5 Week 10

## Finding differences 

How I chose my two tests from the 652 commonmark-spec tests where my implementation  had different answers than the implementation we provided for lab 9:

I ran both with script.sh (below)
![script file](/script.png)

then I saved that to a file called results.txt and compared these results.txt to each other with ```diff``` my result is first and the result of the class code is second.

![running diff](/diffcommand.png)


## Bugs in the two tests

For each test:
Describe which implementation is correct, or if you think neither is correct, by showing both actual outputs and indicating what the expected output is.
For the implementation that’s not correct (or choose one if both are incorrect), describe the _bug (the problem in the code). You don’t have to provide a fix, but you should be specific about what is wrong with the program, and show the code that should be fixed.

## First test

The first one I'm looking at corresponds to test22, my code got 
``` 
test-files/22.md
[/bar\* "ti\*tle"] 
```
while the code from class got
``` 
test-files/22.md
[] 
```
The file 22.md contains

```[foo](/bar\* "ti\*tle") ```

The link contains a space and an asterisk, neither of which should be there, so in this case I think the code from class is correct. Line 75 of the code from class check's that there's not a space in the link before adding and returning it, so I would put all of the code that can return in an if statements that checks that the link does **not** contain a space. The class code used 
```if(potentialLink.indexOf(" ") == -1 ) {}```

and I would put a similar statement around this code:



[Back to home page](index.html)
