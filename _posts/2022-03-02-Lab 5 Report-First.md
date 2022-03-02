---
layout: post
title: Lab 5 Report
subtitle:
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [lab 5]
comments: true
---

##Python and Jupyter Notebook

###Cracking the Questions!

**Question 1: What do you notice about how this function has split the string "Okay, okay, ladies, now let's get in formation, cause I slay"? What has it done that isn't quite right, and why has it done this?
What does the regular expression "\W+" mean in Python? To find this out, you can search the re package documentation. Search the page (command/control + F in a web browser) for the term \W. What does it mean? Do the same for the + sign? What does it do? So what do these symbols mean when used together in a regular expression?** <br/>
In regular expression, “\W” means to match any non-word characters, so in Python, “\W” slices all alphanumeric words by any non-word characters. The + sign indicates to command the function to continue until the condition of the function ends. For example, [ok\W+] from the law string, "Okay, okay, ladies, now let's get in formation, cause I slay," the function matches the two “ok”ays, because there are only two “ok”ays. Here “\W+” splits all alphanumeric words but cannot understand the abbreviated word with an apostrophe such as “let’s” so that’s why “let’s” is divided into “let” and “s”.

**Question 2: What happened? Did it work as you expected? If not, what happened that you didn't expect?** <br/>
My chunk of text is “So let us melt, and make no noise, No tear-floods, nor sigh-tempests move;” from John Donne’s “A Valediction: Forbidding Mourning.” The result was exactly the same with my expectation: the ‘split_into_words’ function does not view “tear-floods” and “sigh-tempests” as one words, so these words linked with dash (-) were divided into. However, interestingly, the function seemed to perceive a semicolon (;) and it was produced into a blank encircled with quotation marks, ‘ ‘; thus, the result became different depending on whether I put a semicolon or not at the end of the sentence as below. <br/>
1-1.	My chunk of text: “So let us melt, and make no noise, No tear-floods, nor sigh-tempests move;” <br/>
1-2. Result: ['so', 'let', 'us', 'melt', 'and', 'make', 'no', 'noise', 'no', 'tear', 'floods', 'nor', 'sigh', 'tempests', 'move', **' '**] <br/>
2-1. My chunk of text: “So let us melt, and make no noise, No tear-floods, nor sigh-tempests move” <br/>
2-2. Result: ['so', 'let', 'us', 'melt', 'and', 'make', 'no', 'noise', 'no', 'tear', 'floods', 'nor', 'sigh', 'tempests', 'move'] <br/>
I also intentionally added other special characters such as a question mark (?), a plus sign (+), and a parenthesis at the end of the line, and the result were the same, ‘ ‘. From the repeated experiments, I found out that any non-word characters were matched only when they were between alphanumeric words, as the ‘split_into_words’ function does not view “let’s” or “tear-floods” as one words. The reason why the non-word characters between word-characters are not recognized is that the function is *to split into words* and it seems that the regular expression “\W” matches all non-alphanumeric words including the spaces between the words, and splits the word-characters by special characters and spaces. Therefore, the function understood the semicolon after the move, “move;”, as a place to divide between “move” and the closing quotation mark (“), and that is why ‘ ‘ became produced.

**Question 3: Describe the output of this script (the dataframe that displays after the above cell finishes running). Remember that this is the same output as the "vir-ver-counts-specific" spreadsheet in our Lab5 Google drive folder, only for just 10 texts. What is this dataframe showing us?**<br/>
The dataframe shows that the table consists of 9 lines. All the data are displayed by the filename (.xml files), the author, the title, the date of publication, and the words either virtu or vertu. The data in the chart are variables that the algorithm commended.

**Question 4: Look at the below lines from the compare_counts_specific function above. These lines use regular expressions to do something to the value of the <date> field in an xml file (if the contents of the <date> field meet certain conditions, that is). What are these lines doing?** <br/>
According to the regular expression syntax:
The general module of regular expression syntax is consisted of “function(r’pattern’, ‘string’)”
Therefore, the module “re.search” indicates to search the string,
the carat sign (^) means the beginning point, that is, “from”
the module “re.sub” signifies to replace the string,
Overall, these lines tell if any string (date) beginning with 20 is found, then it will be replaced to blank, that is, deleted. In other words, the regular expression commands to delete all the dates (probably the year) beginning with 20 from EEBO TCP.mxl files.


![The dubious turtle drawing lines on the screen](_static/images/dsc12_logo.gif)
