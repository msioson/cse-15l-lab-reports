# Week 10: Lab Report 5
***

In this lab report, we will be talking about the differences between the group
implementation and course implementation of MarkdownParse. The tests were found
by running the bash script and selecting the files that led to the course 
implementation to return a link or more.

Expected outputs are to be retried from 
[here](https://spec.commonmark.org/dingus/), the reference CommonMark 
implementation.

## Test File 1: 194.md

The test file that we will be analysing is 
[194.md](Screenshots/lab_report_5/194.md) in both implementations of 
MarkdownParse. 
```
[Foo*bar\]]:my_(url) 'title (with parens)'

[Foo*bar\]]
```

### CSE15L Implementation: 
![Image](Screenshots/lab_report_5/cse15l_1_implementation_194.png)

The output contains a link from within the first line of the Markdown file, 
returning the link from `[Foo*bar\]]:my_(url)`.

### Group Implementation:
![Image](Screenshots/lab_report_5/group_implementation_194.png)

The output from the group implementation of MarkdownParse returned nothing from 
the Markdown test file.

### Expected:
![Image](Screenshots/lab_report_5/194_expected.png)

According to the reference CommonMark implementation, there was indeed an 
expected URL whose address should have been `my_(url)`, not just `url` or 
nothing. This is honestly quite interesting seeing that the `my_` part of it 
was not in the parentheses, however it is expected to be in there so in this 
regard, both implementations are wrong.

#### Potential Solution:

Given that the CSE15L implementation returned `url` from within the parentheses
even though separated from the brackets, the code should be fixed to have it 
account for the square brackets not directly preceding the parentheses and thus
not being considered link.

![Image](Screenshots/lab_report_5/cse15l_method.png)

Although this method appears to find a closing parenthesis, it does not seem as 
though there is a way of determining if those sets of parentheses come right 
after a closing bracket, which could be where the possible solution would go.


## Test File 2:

