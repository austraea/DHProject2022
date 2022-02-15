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

**First Trial**

1. Remove all special characters except for ";, ü, and &"    
RegEx: [^(A-Za-z0-9;&ü)\s]     
Sub: null     
[Output](https://regex101.com/r/qh0rqR/1) 

2. Remove the parentheses     
RegEx: [()]
Sub: null
``````
The Epoch Times New York ed; New York (NY)
La Voz Bilingüe; Denver Colo
Jewish Advocate; Boston
Washington Informer; Washington DC
News from Indian Country; Hayward WI
Afro  American 5 Star edition; Baltimore Md
Diverse Issues in Higher Education; Fairfax Virginia
The Gay &amp; Lesbian Review Worldwide; Boston MA
The Hispanic Outlook in Higher Education; Paramus NJ
``````


1. Remove all the special characters except for “;, ü, and &”     
RegEx: [^(A-Za-z0-9;&ü)\s]     
Sub: null<br/>
```
The Epoch Times New York ed; New York (NY)
La Voz Bilingüe; Denver Colo
Jewish Advocate; Boston
Washington Informer; Washington DC
News from Indian Country; Hayward WI
Afro  American 5 Star edition; Baltimore Md
Diverse Issues in Higher Education; Fairfax Virginia
The Gay &amp; Lesbian Review Worldwide; Boston MA
The Hispanic Outlook in Higher Education; Paramus NJ
```

2. Remove the parentheses<br/>
RegEx: [()]<br/>
Sub: null<br/>
```
The Epoch Times New York ed; New York NY
La Voz Bilingüe; Denver Colo
Jewish Advocate; Boston
Washington Informer; Washington DC
News from Indian Country; Hayward WI
Afro  American 5 Star edition; Baltimore Md
Diverse Issues in Higher Education; Fairfax Virginia
The Gay &amp; Lesbian Review Worldwide; Boston MA
The Hispanic Outlook in Higher Education; Paramus NJ
```

3.
