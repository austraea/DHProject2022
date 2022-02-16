---
layout: post
title: Lab 3 Report
subtitle:
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [lab 3]
comments: true
---

## Magical World of RegEx

Working with the Sample Dataset
-------------------------------

Dealing with the Regular Expression program required a persistent and experimental mind. Before “cleaning” or “tidying” dataset sample, I read Professor Thomas’s instructions on the course website twice carefully and watched tutorial videos. Confused but bravely, I combined as many regexes as possible from a single letter to ([multiple letters, numbers, and characters]), employed basic matchings and characters, and input them into the “Regular Expression box.” Fortunately, the regexes I input into the box worked!
I did not venture into cracking the codes right after my initial practices. I did more experiments: removing information before or after the semicolon. For instance, I input ``(.*)\;`` or ``\;(.*)`` to remove information before or after the semicolon as follows.
[Output Ex1.]( https://regex101.com/r/uAZVT9/1)
[Output Ex2.]( https://regex101.com/r/cZwgGI/1)
It was time-consuming, yet it was worth a shot! This process allowed me to become familiar with the Regular Expression program.
The following records demonstrate my attempts to clean the dataset. What I focused on was how to remove as many characters as possible at once. After several trials and errors, I found (sometimes unexpectedly!) possible solutions. 

**First Attempt**

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

6. Remove dash in "Afro - American"<br/>
RegEx: -(space)
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
a. RegEx: amp,         
[Output 9.a](https://regex101.com/r/l9F2Fl/1)     

**Second Attempt**
In my second attempt, I input different regex expressions from the one in my first attempt.

1. Remove all special characters except for “; and &”    
RegEx:<br/>
  a. [,.(\)"[\]?] or<br/>
  b. [_%+,."?[\]()]+     
[Output 1.a.](https://regex101.com/r/1jlfvl/1)      
[Output 1.b.](https://regex101.com/r/EDciXI/1)    

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

5. Remove dash in "Afro - American"<br/>
RegEx: -(space)

6. Substitute “Md” to “MD”    
RegEx: Md    
Sub: MD    

7. Substitute “Virginia” to “VA”       
RegEx: Virginia    
Sub: VA    

8. Remove “amp,”    
RegEx: amp,    
