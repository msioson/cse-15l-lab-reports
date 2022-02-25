# Week 8: Lab Report 4

## MarkdownParse Testing
***
For lab report 4, there are three markdown snippets that will be used to test
our implementations of MarkdownParse. Those snippets being:

[Snippet 1](https://raw.githubusercontent.com/msioson/cse-15l-lab-reports/master/Screenshots/lab_report_4/snippet-1.md)

CommonMark demo:

![Image](Screenshots/lab_report_4/snippet1.png)

[Snippet 2](https://raw.githubusercontent.com/msioson/cse-15l-lab-reports/master/Screenshots/lab_report_4/snippet-2.md)

CommonMark demo:

![Image](Screenshots/lab_report_4/snippet2.png)

[Snippet 3](https://raw.githubusercontent.com/msioson/cse-15l-lab-reports/master/Screenshots/lab_report_4/snippet-3.md)

CommonMark demo:

![Image](Screenshots/lab_report_4/snippet3.png)

Since these snippets are being used to test our implementations of 
MarkdownParse, JUnit will be used to test them.

![Image](Screenshots/lab_report_4/markdownparsetest.png)

### My Implementation

[My Implementation of Markdown Parse](https://github.com/msioson/markdown-parse/tree/lab_report_4_snippets)

Resulting test of all three snippets:
![Image](Screenshots/lab_report_4/errorsofmyimplementation.png)

None of the tests passed.

### Reviewed Implementation

[Reviewed Implementation of Markdown Parse](https://github.com/atruong39/markdown-parse)

Resulting test of all three snippets:
![Image](Screenshots/lab_report_4/reviewedimplementationtests.png)

None of the tests passed as well.

## Questions
***

- Snippet 1
  - There may be a small code change that would make my programme work with the 
1st snippet; because the code worked well with getting the links, it's more a 
matter of excluding the first one as it seems like the backtick made the first 
link excluded in the CommonMark demo. So a possible, but short, fix would be to 
exclude links whose titles within brackets are inside of code blocks, perhaps by
determining if the brackets are surrounded or within backticks.
- Snippet 2
  - For snippet 2, there might not be a small code change that would make my
programme work with it. According to the CommonMark demo, the only link included
within the nested loop was the innermost link, but my code works in a way where 
it only works with the outer set of parentheses and, and thus links. So the 
code change for this would be a lot more, though still very much possible.
- Snippet 3
  - Lastly for snippet 3, there seems to be a small code change what would get
my programme to work with it. In which case, there are two links when there 
should only be one according the CommonMark demo. Now understanding the reason, 
the extra, empty line break between the lines for the first link is why it was 
excluded in the CommonMark demo. Using this reasoning, we can modify the code to 
still allow for links with line breaks, but exclude links with an extra, empty
line break where the CommonMark demo otherwise excluded it. This can be done by
looking for two line breaks or more next to each other and make it not include
that same link in the list.
