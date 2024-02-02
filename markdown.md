# Markdown
Markdown is a popular "markup" language used all over the internet.
A markup language is just a system for describing the formatting of text.
Examples include html and TeX.
Markdown is great because it is very simple, and both the original text file and the resulting html or pdf created from it are clear and easy to read.

# GitHub and Markdown
GitHub will automatically display Markdown files after processing.
The same goes for GitHub issues and discussions.
So in general, for any repo file that is meant to contain descriptive text (not data, not code), consider using a Markdown file.

# Creating a Markdown file
To make a Markdown file just create a new text file and give it the `.md` extension.

# Markdown syntax
Markdown can be really simple.
For our work, the few types of syntax shown below are all you need in most cases.

```
# Main heading
Regular text about something.

## Heading level 2
Putting each sentence on a separate line is a good idea.
That lets Git track changes more precisely.

### Heading level 3

Here is a list:

* Item 1
* Item 2
* Item 3

Or number it:

1. First
2. Second
3. Something else


**bold** or *italics*

`code` syntax is also handy for file paths sometimes.

<URL> e.g., <https://www.markdownguide.org/basic-syntax/>

or [links](https://www.markdownguide.org/basic-syntax/)
```

After processing, this plain text will be displayed like this:

# Main heading
Regular text about something.

## Heading level 2

### Heading level 3

Here is a list:

* Item 1
* Item 2
* Item 3

Or number it:

1. First
2. Second
3. Something else


**bold** or *italics*

`code` syntax is also handy for file paths sometimes.

<URL> e.g., <https://www.markdownguide.org/basic-syntax/>

or [links](https://www.markdownguide.org/basic-syntax/)

See the link above for more details.
One more thing that is useful: use three backtick quotes for code blocks:

```

\```
x <- mean(1:3)
x / 2
\```

```
