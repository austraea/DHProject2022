---
layout: post
title: Lab 4 Report
subtitle:
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [lab 4]
comments: true
---

## Data Analysis and Voyant

<br/>
### Exploring Voyant

**Question 1: How does this change the word cloud, and what are these changes telling you?**<br/>
Before “stopwords” was set to “auto-detect,” the words such as “students,” “said,” and “humanities” were ordered by frequency; but when the “none” button was selected in the options box, articles (the), prepositions (of), and conjunctions (and) were listed, instead. However, these “stopwords” are commonly used in English sentences without any meaning. That is, these words do not provide any meaningful or essential information to the audience.

**Question 2: Why is relative frequency sometimes a more useful or accurate measure of a term’s importance than raw frequency?**<br/>
Raw frequency tells the total count of one term *in the entire corpus*. The word “student” is counted 3359 in all documents uploaded into Voyant, but its most frequency does not guarantee that the word “students” is regarded as important in the whole documents because this term is not always considered to be significant throughout the whole documents; instead, the term would not be used at all in some documents. On the contrary, relative frequency shows the total count of one term *in one document*, that is, the proportion of the term used/mentioned in one document. The more important one term is, the more frequently it is mentioned in one/certain document. Therefore, relative frequency is more effective in showing one term’s importance.

**Question 3: What is this document? And, more importantly, what have you learned about the term “mcas” in our corpus overall, and/or the utility or value of “significance” metrics like TF-IDF?**<br/>
The term “mcas” appears in document #442, and this document is a letter urging to guarantee full-time employment for all Honor professionals who might lose their jobs due to the termination of Morrissey College of Arts and Sciences honors programs. After the letter, there follows a list of students or faculty members who are assumed to support what the writer urges. The term “mcas” comes between each student or faculty member’s name and year of admission or graduation. Considering the school’s name, Morrissey College of Art Science, it can be presumed that “mcas” might refer to the acronym of the school’s name. In this document, “mcas” does not seem significant because it does not contain any specific and important meaning or information; rather, the TF-IDF score measures its significance because of the term’s repetition throughout the document. Therefore, the TF-IDF score needs to be carefully used.

**Question 4: Looking through this list of terms and their “Comparison” values, what observations can you make about terms that are more likely to occur in the humanities corpus vs. terms that are more likely to occur in the science corpus? How are these terms different?**<br/>
The tables below show the order of the term’s relative frequency in the Humanities and Science corpora.

* Humanities Corpus

|  Term | Comparison |
| :-----| :---|
| student | 0.00630 |
| humanities | 0.00545 |
| faculty | 0.00241 |
| studies | 0.00238 |
| courses | 0.00220 |
| course | 0.00214 |
| history | 0.00209 |
<br/>

* Science Corpus

|  Term | Comparison |
| :-----| :---|
| science | -0.00254 |
| research | -0.00224 |
| researchers | -0.00147 |
| scientists | -0.00145 |
| health | -0.00120 |
| cancer | -0.00109 |
| data | -0.00093 |

As the tables show, in the humanities corpus, the terms “student,” “humanities,” “faculty,” “studies,” “course(s),” and “history” are listed. These terms are mainly related to education. On the contrary, in the science corpus, the terms such as “science,” “research,” “researchers,” “scientist,” “health,” “cancer,” and “data” are presented, which more focus on research. Also, compared to the differences between the term’s relative frequency in both corpora, the data in humanities corpus contain more abstract words, such as “humanities,” and “studies”; the terms in the science corpus are more specific, like “cancer” and “data.”

**Question 5: What tool(s) did you explore? What did this tool(s) help you to observe about this data and/or what did you learn about this data using this tool(s)? Alternatively, what did you hope to learn about this data using this tool and how (or why) did reality seem to fall short of that expectation?**<br/>


<br/>
### After Exploratory Data Analysis
