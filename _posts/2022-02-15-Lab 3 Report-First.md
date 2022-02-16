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




**First Attempt**

1. Remove all special characters except for “;, ü, and &”    
RegEx: [^(A-Za-z0-9;&ü)\s]    
[Output 1](https://regex101.com/r/qh0rqR/1)

2. Remove the parentheses    
RegEx: [()]      
[Output 2](https://regex101.com/r/tILcdu/1)

3. Substitute “;” to “,”    
RegEx: ;    
Sub: ,    
[Output 3](https://regex101.com/r/JvgoiQ/1)

4. Substitute “Colo” to “CO”    
RegEx: Colo    
Sub: CO    

5. Substitute “Boston” to “Boston MA”    
RegEx: Boston    
Sub: Boston MA    
`in this case, turn off the RegEx Flags, g and m`       
[Output 5](https://regex101.com/r/gp0iSK/1)<br/>       

6. Substitute "Afro  American" to "Afro American"    
RegEx: Afro  American    
Sub: Afro American

7. Substitute “Md” to “MD”    
RegEx: Md    
Sub: MD    

8. Substitute “Virginia” to “VA”       
RegEx: Virginia    
Sub: VA    

9. Remove “amp,”    
RegEx: amp,      
[Output 9](https://regex101.com/r/cLNMk8/1)     


**Second Attempt**

1. Remove all special characters except for “; and &”    
RegEx:<br/>
  a. [,.(\)"[\]?] or<br/>
  b. [_%+,."?[\]()]+    
Sub: null      
[Output 1.a.](https://regex101.com/r/1jlfvl/1)      
[Output 1.b.](https://regex101.com/r/EDciXI/1)    

2. Substitute “;” to “,”    
RegEx: ;    
Sub: ,    
[Output 2](https://regex101.com/r/JvgoiQ/1)        

3. Substitute “Colo” to “CO”    
RegEx: Colo    
Sub: CO    

4. Substitute “Boston” to “Boston MA”    
RegEx: Boston    
Sub: Boston MA    
`in this case, turn off the RegEx Flags, g and m`       
[Output 5](https://regex101.com/r/gp0iSK/1)<br/>       

5. Substitute "Afro  American" to "Afro American"     
RegEx: Afro  American     
Sub: Afro American     

6. Substitute “Md” to “MD”    
RegEx: Md    
Sub: MD    

7. Substitute “Virginia” to “VA”       
RegEx: Virginia    
Sub: VA    

8. Remove “amp,”    
RegEx: amp,    
