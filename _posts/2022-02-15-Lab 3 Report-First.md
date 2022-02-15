---
layout: post
title: Lab 3 Report
subtitle:
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [lab 3]
comments: true
---

### Magical World of RegEx
First Trial
1. Remove all special characters except for “;, ü, and &”

RegEx: [^(A-Za-z0-9;&ü)\s]

Sub: null

`````
The Epoch Times New York ed; New York (NY)
La Voz Bilingüe; Denver Colo
Jewish Advocate; Boston
Washington Informer; Washington DC
News from Indian Country; Hayward WI
Afro  American 5 Star edition; Baltimore Md
Diverse Issues in Higher Education; Fairfax Virginia
The Gay &amp; Lesbian Review Worldwide; Boston MA
The Hispanic Outlook in Higher Education; Paramus NJ
`````

2. Remove the parentheses

RegEx: [()]

Sub: null

`````
`````


3. Substitute “;” to “,”
RegEx: ;
Sub: ,


4. Substitute “Colo” to “CO”
RegEx: Colo
Sub: CO


5. Substitute “Boston” to “Boston MA”
RegEx: Boston
Sub: Boston MA
* in this case, turn off the RegEx Flags, g and m


6. Substitute “Md” to “MD”
RegEx: Md
Sub: MD


7. Substitute “Virginia” to “VA”
RegEx: Virginia
Sub: VA

8. Remove “amp,”
RegEx: amp,
Sub: null

Second Trial
1. Remove all special characters except for “; and &”
1-1. RegEx: [,.(\)"[\]?]
Sub: null
https://regex101.com/r/1jlfvl/1

1-2. [_%+,."?[\]()]+
Sub: null
https://regex101.com/r/EDciXI/1

2. Substitute “;” to “,”
RegEx: ;
Sub: ,
https://regex101.com/r/JvgoiQ/1

3. Substitute “Colo” to “CO”
RegEx: Colo
Sub: CO

4. Substitute “Boston” to “Boston MA”
RegEx: Boston
Sub: Boston MA
* in this case, turn off the RegEx Flags, g and m
https://regex101.com/r/wBWjt1/1

5. Substitute “Md” to “MD”
RegEx: Md
Sub: MD

6. Substitute “Virginia” to “VA”
RegEx: Virginia
Sub: VA

7. Remove “amp,”
RegEx: amp,
Sub: null
https://regex101.com/r/ptHWbD/1
