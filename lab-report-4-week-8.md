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

![test](/test1.png)

# Snippet 2

Test in mdparsetest.java:
pass/**no pass**

![test](/snippet2test.png)

My implementation's output: 

![test](/snippet2myresult.png)

Reviewed implementation's output: 

![test](/test1.png)

# Snippet 3

Test in mdparsetest.java:
pass/**no pass**

![test](/snippet3test.png)

My implementation's output: 

![test](/snippet3myresult.png)

Reviewed implementation's output: 

![test](/test1.png)

# Questions
Answer the following questions with 2-3 sentences each:

1. Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

2. Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.

3. Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.

[Back to home page](index.html)



## Snippet 1

`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)

## Snippet 2

[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)

## Snippet 3

[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
    https://ucsd-cse15l-w22.github.io/
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
