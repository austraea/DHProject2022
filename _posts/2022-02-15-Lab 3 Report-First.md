---
layout: post
title: Lab 3 Report
subtitle:
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [lab 3]
comments: true
---

## Magical World of Regular Expressions

<br/>
### "Cleaning" the Dataset Sample

Dealing with the Regular Expression program required a persistent and experimental mind. Before “cleaning” or “tidying” dataset sample, I read Professor Thomas’s instructions on the course website twice carefully and watched tutorial videos. Confused but bravely, I combined as many regexes as possible from a single letter to ([multiple letters, numbers, and characters]), employed basic matchings and characters, and put them into the “Regular Expression box.” Fortunately, the regex syntax I input the box was valid!
I did not venture into cracking the codes right after my initial exercises, yet. I conducted more experiments: removing some field of the data before or after the semicolon. For instance, I input ``(.*)\;`` or ``\;(.*)`` to remove a field of the data before or after the semicolon as follows.<br/>
* [Output Ex1.]( https://regex101.com/r/uAZVT9/1)<br/>
* [Output Ex2.]( https://regex101.com/r/cZwgGI/1)<br/>

It was time-consuming, yet it was worth a shot! This process allowed me to become familiar with the Regular Expression program.<br/>
The following records demonstrate my attempts to clean the dataset. What I focused on was how to remove as many characters as possible at once. After several trials and errors, I found (sometimes unexpectedly!) possible solutions, and finally, the time to crack the codes came!

**First Attempt**<br/>
In my first attempt, I focused on how to remove the parentheses and the brackets together, which I had not found any solutions yet. So I started my task with removing those special characters separately.

1. Remove all special characters except for “-, ;, ü, and &”    
RegEx: [^(A-Za-z0-9-;&ü)\s]    
[Output 1](https://regex101.com/r/ac9HBV/1)

2. Remove the parentheses    
RegEx: [()]      
[Output 2](https://regex101.com/r/rXPW9j/1)

3. Substitute “;” to “,”    
RegEx: ;    
Sub: ,    
[Output 3](https://regex101.com/r/ZlrgIo/1)

4. Substitute “Colo” to “CO”    
RegEx: Colo    
Sub: CO    
[Output 4](https://regex101.com/r/UvsWBU/1)

5. Substitute “Boston” to “Boston MA”    
RegEx: Boston    
Sub: Boston MA    
`in this case, turn off the RegEx Flags, g and m`       
[Output 5](https://regex101.com/r/7POPJT/1)<br/>       

6. Remove the dash in "Afro - American"<br/>
RegEx: -(space)<br/>
[Output 6](https://regex101.com/r/QpAJ3y/1)

7. Substitute “Md” to “MD”    
RegEx: Md    
Sub: MD    
[Output 7](https://regex101.com/r/nOiTl5/1)

8. Substitute “Virginia” to “VA”       
RegEx: Virginia    
Sub: VA    
[Output 8](https://regex101.com/r/SoN9MF/1)

9. Remove “amp,”    
RegEx: amp,         
[Output 9](https://regex101.com/r/l9F2Fl/1)     

**Second Attempt**<br/>
In my second attempt, I input different regexes from that in my first attempt.

1. Remove all special characters except for “; and &”    
RegEx:<br/>
  a. [,.(\)"[\]?] or<br/>
  b. [_%+,."?[\]()]+     
[Output 1.a.](https://regex101.com/r/1jlfvl/1)      
[Output 1.b.](https://regex101.com/r/EDciXI/1)    
`Make sure to add a slash inside the parentheses and the brackets`

2. Substitute “;” to “,”    
RegEx: ;    
Sub: ,     

3. Substitute “Colo” to “CO”    
RegEx: Colo    
Sub: CO    

4. Substitute “Boston” to “Boston MA”    
RegEx: Boston    
Sub: Boston MA    
`in this case, turn off the RegEx Flags, g and m`          

5. Remove the dash in "Afro - American"<br/>
RegEx: -(space)

6. Substitute “Md” to “MD”    
RegEx: Md    
Sub: MD    

7. Substitute “Virginia” to “VA”       
RegEx: Virginia    
Sub: VA    

8. Remove “amp,”    
RegEx: amp,    

<br/>
### After Data Cleaning

Before the Regular Expressions, I was unable to figure out the concept of “cleaning” data. How can the researchers or programmers “clean” dataset or data? Moreover, what is “cleaning” dataset or data? (This series of question reveal how I have been unfamiliar with Digital & Data Science!) Consider all the datasets we have worked with for two weeks: both HathiTrust dataset and this week’s raw dataset are “messy” and “dirty”, and they need to be (re)edited or (re)organized for later use. My impression of these datasets, however, is not far from what Katie Rawson and Trevor Muñoz point out in "Against Cleaning":

> [Data cleaning] is understood as a step that inscribes *a normative order* by wiping away what is different. The term “cleaning” implies that a dataset begins as “messy.” “Messy” suggests an underlying order: it supposes things already have a rightful place, but they are not in it [.]

The ideas of “messy” data and its (re)organization are parts of the paradigm of “‘correct’ order” (Rawson and Muñoz). This paradigm does not allow any differences, i.e., no diversity of data. At this moment, I recollected what I pointed out in my [Lab 2 Report](https://austraea.github.io/2022-02-09-Lab-2-Report-Second/). I said,

> [Some] data is unorganized, so they are invalid to be used and analyzed. For instance, “China, Shanghai (China),” “Nanjing (Jiangsu Shen, China)” should be labeled under “China”; “Ginza (Tokyo, Japan)” should be under “Japan.” Therefore, I wonder whether the dataset and the whole data are valid for further research.

I might have too focused on the dataset’s “tidiness” and its normative structure or pattern that we generally have accepted. In this “messy” dataset, “there is actually rich information about the circumstances under which it was collected” (D’lgnazio and Klein)[^1]. The data such as “Nanjing (Jiangsu Shen, China)” or “Ginza (Tokyo, Japan)” could inform us about the researchers, their perspectives, and the social and historical background when the data was collected to create the HathiTrust dataset. Also, we could ask a question, “why does the city (Nanjing) or district (Ginza) come first in the publication venue information?” or “why is there no data containing the information about provinces or cities in Korea within it?” Likewise, these processes of handling “messy” datasets allow us to expand our insights and preserve diversity within the datasets.

This week’s lab with Regular Expressions, however, seems to be far from the general and ordinary concept of data cleaning process. Of course, we were to make the “messy” dataset tidy, and we were to separate columns, remove chaotic characters, and standardize the patterns. The whole process, nevertheless, is near to an experimental journey to search for a variety of resolutions, not a process of placing the dataset within a hierarchical, normative, and correct order. I removed “amp;” from the raw dataset contrary to the dataset we are given in .csv format, which would create differences in our dataset and data within it. Furthermore, our own dataset would be shared with, revised, and employed by ENG 612 members (or beyond the class!) as the Data-Sitters Club. All the processes we have undertaken and will take might be a journey toward “transparency” in data science and the data for “co-liberation.”

[^1]: D'Ignazio, Katherine and Lauren Klein. "Unicorns, Janitors, Ninjas, Wizards, and Rock Stars," *Data Feminism*, 2020.
