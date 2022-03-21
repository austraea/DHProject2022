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
I explored various tools in Voyant program. Among them, I became enamored with Dreamspace tool through which the text is represented geospatially. For instance, when I worked with Thomas Malory’s *Le Morte d’Arthur*, it showed the patterns of recurring travels in the text, the knight-errants’ journeys. So, I could see how a particular knight travels through the country or abroad in the text. Dreamspace would be an effective tool in that it can show the patterns of traveling of people, ideas, and goods, through which scholars and researchers can trace back how certain people or items migrate and deduce its consequences; they can discover and construct the narratives of traveling of items that have been ignored like slave trades. However, although its function of automatically identifying locations, it is imperfect. That is, the tool identifies the locations but cannot understand whether the term refers to either geographical location or others. For instance, working with *Le Morte d’Arthur*, the tool understands <span style="color: lightcoral;">Sir Lucan</span>, one of the knights in the text, as <span style="color: lightcoral;">a place in Ireland</span>. Also, this tool is based on real geographical references, so the imaginative places cannot be represented with this tool. Nevertheless, it is sure that Dreamspace is quite a fascinating tool to decipher texts with geospatial images.

![Dreamspace](img/Dreamspace_1.jpg)

The second tool I explored is Trends that “shows a line graph depicting the distribution of a word’s occurence across a corpus and document.” The function of Trends is similar to that of StreamGraph, which visualizes “the change of the frequency of words in a corpus.” However, it is not easy to decipher how certain keywords are frequently used with StreamGraph, Trends indicates the exact number of raw or relative frequencies in the document. The Trends tool has several options to change chart mode and show labeled keywords. Also, the users can change the number of the segment in the document or corpus. With this tool, scholars and researchers can trace back how and why certain keywords in the certain segment of the text were used more or less frequently than others; why certain terms in a certain period were used more or less than in another period. This tool will be useful to understand the history of certain terms as Daniel Rosenberg does with the word, data, within certain texts or corpus[^1].  

<br/>
### After Exploratory Data Analysis

Exploring Voyant was somewhat a baffling yet completely amazing experience. When my first trial with Voyant, I uploaded Malory’s *Le Morte d’Arthur*, and waited a little bit. And Voila! The result Voyant brought was thrilling. Both cirrus and trend panels showed visualized texts: the Cirrus panel presented individual words with different sizes according to how each word is frequently referred to; the Trend panel exhibited a graph of relative frequency of words. Voyant tools shift the texts to various forms of images, which most book-worm humanists rarely have experienced; the visualized images shown on Voyant tools definitely present a whole new world to the humanists. Along with visualizing the texts, its counting word frequencies would provide the novice Digital Humanists and others with new approaches, interpretations, and perspectives; opportunities to find out what they might have missed and not recognized yet. Therefore, it would enable further investigations from the existing research in case when the researchers use data or corpora built by others. Sarah Allison claims that although recycling and “re-analyzing someone else’s data [...] poses real challenges to the current value placed on originality” (3) and might be understood as “stealing someone else’s work” (4), this approach offers the paths to the completely new and different research from the original one(s) by researchers’ exploring “an unexplored object that deserves attention” (3).[^2] Not only new academic research through data recycling. Using already built data or corpora offers open-end studies that allow academic collaborations in the field of humanities studies.

Of course, Voyant does not have only merits promising a rosy future to literary research. Voyant’s major function, providing data regarding the word frequencies, teaches us exactly what D’Ignazio and Klein point out throughout their article [^3]. Debunking Chris Anderson’s claim that “the numbers speak for themselves,” these two scholars argue that what is important in data science is not the number(s) but context(s) that can expound how the number(s) have been deducted. That is, the number does not show the whole story. We can find related examples in Voyant. First, from my first trial of Voyant with Malory’s text, I found out that the words “sir,” “said,” and “ye” are repeatedly mentioned. Of course, *Le Morte d’Arthur* is a fifteenth-century text, so that explains why “sir” and “ye” are frequently said (according to *Oxford English Dictionary*, “ye” was used as a pronoun indicating “you”). What else? There are so many knights or male aristocrats in this text and conversations between or among the characters. Yes, it is a chivalric romance! No more new discovery. Another example: the word “mcas.” As we already discussed in question 3, the term “mcas” does not have any meaning in the document where it is frequently mentioned.

Regardless of this point, Voyant is such an interesting tool, and I expect to use it for my future research.

[^1]: Rosenberg, Daniel. “Data Before the Fact,” *“Raw Data” is an Oxymoron*, 2013.
[^2]: Allison, Sarah. “Other People’s Data: Humanities Edition,” *Journal of Cultural Analytics*, 2016.
[^3]: Catherine D’Ignazio and Lauren F. Klein, “The Numbers Don’s Speak for Themselves,” *Data Feminism*, 2020.
