---
layout: post
title: Lab 5 Report
subtitle:
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [lab 5]
comments: true
---

## Python and Jupyter Notebook

<br/>
### Cracking the Questions!

**Question 1: What do you notice about how this function has split the string "Okay, okay, ladies, now let's get in formation, cause I slay"? What has it done that isn't quite right, and why has it done this?
What does the regular expression "\W+" mean in Python? To find this out, you can search the re package documentation. Search the page (command/control + F in a web browser) for the term \W. What does it mean? Do the same for the + sign? What does it do? So what do these symbols mean when used together in a regular expression?** <br/>
In regular expression, “\W” means to match any non-word characters, so in Python, “\W” slices all alphanumeric words by any non-word characters. The + sign indicates to command the function to continue until the condition of the function ends. For example, [ok\W+] from the law string, "Okay, okay, ladies, now let's get in formation, cause I slay," the function matches the two “ok”ays, because there are only two “ok”ays. Here “\W+” splits all alphanumeric words but cannot understand the abbreviated word with an apostrophe such as “let’s” so that’s why “let’s” is divided into “let” and “s”.

**Question 2: What happened? Did it work as you expected? If not, what happened that you didn't expect?** <br/>
My chunk of text is “So let us melt, and make no noise, No tear-floods, nor sigh-tempests move;” from John Donne’s “A Valediction: Forbidding Mourning.” The result was exactly the same with my expectation: the ‘split_into_words’ function does not view “tear-floods” and “sigh-tempests” as one words, so these words linked with dash (-) were divided into. However, interestingly, the function seemed to perceive a semicolon (;) and it was produced into a blank encircled with quotation marks, ‘ ‘; thus, the result became different depending on whether I put a semicolon or not at the end of the sentence as below. <br/>

1-1.	My chunk of text: “So let us melt, and make no noise, No tear-floods, nor sigh-tempests move;” <br/>
1-2. Result: ['so', 'let', 'us', 'melt', 'and', 'make', 'no', 'noise', 'no', 'tear', 'floods', 'nor', 'sigh', 'tempests', 'move', **' '**] <br/>
2-1. My chunk of text: “So let us melt, and make no noise, No tear-floods, nor sigh-tempests move” <br/>
2-2. Result: ['so', 'let', 'us', 'melt', 'and', 'make', 'no', 'noise', 'no', 'tear', 'floods', 'nor', 'sigh', 'tempests', 'move'] <br/>

I also intentionally added other special characters such as a question mark (?), a plus sign (+), and a parenthesis at the end of the line, and the results were the same, ‘ ‘. From the repeated experiment, I found out that any non-word characters were matched only when they were between alphanumeric words, as the ‘split_into_words’ function does not view “let’s” or “tear-floods” as one word. The reason why the non-word characters between word characters are not recognized is that the function is *to split into words* and it seems that the regular expression “\W” matches all non-alphanumeric words, including the spaces between the words, and splits the word characters by special characters and spaces. Therefore, the function understood the semicolon after the move, “move;”, as a place to divide between “move” and the closing quotation mark (”), and that is why ' ' became produced.

**Question 3: Describe the output of this script (the dataframe that displays after the above cell finishes running). Remember that this is the same output as the "vir-ver-counts-specific" spreadsheet in our Lab5 Google drive folder, only for just 10 texts. What is this dataframe showing us?**<br/>
The dataframe shows that the table consists of 9 lines. All the data are displayed by the filename (.xml files), the author, the title, the date of publication, and the words either virtu* or vertu*. The data in the chart are variables that the algorithm commended.

**Question 4: Look at the below lines from the compare_counts_specific function above. These lines use regular expressions to do something to the value of the <date> field in an xml file (if the contents of the <date> field meet certain conditions, that is). What are these lines doing?** <br/>

According to the regular expression syntax:

1. The general module of regular expression syntax is consisted of “function(r’pattern’, ‘string’).”
2. Therefore, the module “re.search” indicates to search the string,<br/>
3. the carat sign (^) means the beginning point, that is, “from”<br/>

Overall, these lines tell if any string (date) beginning with 20 is found, then it will be replaced to blank, that is, deleted. In other words, the regular expression commands to delete all the dates (probably the year) beginning with 20 from EEBO TCP.mxl files.

<br/>
### After Exploring the World of Python and Jupyter Notebook

Week after week, I have learned various high-tech tools and skills from Regular Expression, Voyant, and finally to Python and Jupyter Notebook. As a person whose heart easily throbs by looking at shiny and high-tech things, I have been unable to resist any temptations from those unknown worlds of computer programming knowledge and skills; simultaneously, the more concepts and program syntax have been introduced to me, the more often I feel that all knowledge and skills have come to me so quickly. Although armed with an adventurous spirit, I am still worried about not fully understanding the principles of the programs or being an expert of none of them: “I have just understood how Regular Expressions work and still need more practice. I am still inept for Regular Expression. But I need to employ it to other programs!”

However, the Data-Sitters Club members’ coding stories whispered to me that the members had not been experts at all from the beginning. They learned coding and programming languages only when they needed them. For instance, Katherine Bowers (Katia) and her colleagues of Team Dostoevsky learned “some basic XML” to use TEI; and in order to do something with XML, they took DHSI class where they could familiarize with other programs such as XPath, XQuery, and SXLT. They do not need to master all the programs they need. Roopika Risam (Roopsi) says that she is “still use out-of-box tools when the situation calls for it.”[^1] Remember Hyekyung, “out-of-box tools”! Theses digital humanities, moreover, choose as easy tools as they can. Roopsi says that “more recently when I chose to build a WordPress page […] rather than a Jekyll site to make life easier for a group of collaborators.”[^2] How cool they are! Their stories are not far from what Benjamin M. Schdmidt argues in his article, “Do Digital Humanists Needs to Understand.” He says that,

> [Digital] humanists do not need to understand algorithms at all. They do need, however, to understand the transformations that algorithms attempt to bring about. If we do so, our practice will be more effective and more likely to be truly original.[^3]

What matters for digital humanists when they work with data is how the transformations (the results) could be understood and interpreted, rather than how the transformations have been created.  As a future digital humanist, what I focus on is not how the programs works nor how my ineptitude for the programming impedes my DH projects, but *what the program produces*.


[^1]: Bowers, Katherine, Quinn Dombrowski, and Roopika Risam, “DSC #12: The DSC and the New Programming Language,” *The Data-Sitters Club*, 2021.

[^2]: Bowers, Katherine, Quinn Dombrowski, and Roopika Risam, “DSC #12: The DSC and the New Programming Language,” *The Data-Sitters Club*, 2021.

[^3]: Schmidt, Benjamin M. “Do Digital Humanists Need to Understand Algorithms?” *Debates in the Digital Humanities*, 2016
