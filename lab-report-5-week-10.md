# Lab Report 5 Week 10

## Finding differences 

How I chose my two tests from the 652 commonmark-spec tests where my implementation  had different answers than the implementation we provided for lab 9:

I ran both with script.sh (below)
![script file](/script.png)

then I saved that to a file called results.txt and compared these results.txt to each other with ```diff``` my result is first and the result of the class code is second.

![running diff](/diffcommand.png)


## Bug 1

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

The link contains a space and an asterisk, neither of which should be there, so in this case I think the code from class is correct. Line 75 of the code from class checks that there's not a space in the link before adding and returning it, so I would put all of the code that can return in an if statement that checks that the link does **not** contain a space. The class code used 
```if(potentialLink.indexOf(" ") == -1 ) {}```

and I would put a similar statement around this code:

![fix1](/fix1.png)

# Bug 2

The difference is with test 577, this is what's in the test file:
```
!(foo)[train.jpg]
```
My code added train.jpg which shouldn't be added since it's an image.
```
> [train.jpg]
1069c1066
< []
```

The solution to this is to add an if statement to check if there is a ! before the open parentheses. We have code to check for this, but it currently looks at if there's a ! before the open bracket, when it should check before the open parentheses. To fix this issue in the following code I would replace openBracket with openParentheses.

![fix2](/fix2.png)

[Back to home page](index.html)
