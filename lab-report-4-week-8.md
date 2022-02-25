# Lab Report 4 Week 8


# Links

My markdown parse repositry:
[my md parse](link.html)

Reviewed markdown parse repository:
[review md parse](/copyDirect2.png)

# Snippet 1

Test in mdparsetest.java:
pass/**no pass**

![test](/snippet1test.png)

My implementation's output: 

![test](/snippet1myresult.png)

Reviewed implementation's output: 

![test](/snippet1reviewresult.png)

# Snippet 2

Test in mdparsetest.java:
pass/**no pass**

![test](/snippet2test.png)

My implementation's output: 

![test](/snippet2myresult.png)

Reviewed implementation's output: 

![test](/snippet2reviewresult.png)

# Snippet 3

Test in mdparsetest.java:
pass/**no pass**

![test](/snippet3test.png)

My implementation's output: 

![test](/snippet3myresult.png)

Reviewed implementation's output: 

![test](/snippet3reviewresult.png)

# Questions
Answer the following questions with 2-3 sentences each:

1. Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

Yes, I think we should check if there are backticks anywhere in the line. This could be similar to the implementation to make sure images don't count as links with !, if there is a backtick we disregard anything until the next backtick.

2. Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.

No I think it would be more complicated since we currently have code to deal with one set of parentheses and brackets but this would have to deal with an unknown number of them. We would have to store information about each and they could be in any order and be a lot of them.

3. Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.

Yes, I think we could remove any line breaks that are inside of parenthese or brackets where there is an open and close. This way we would be able to get the expected output.

[Back to home page](index.html)
