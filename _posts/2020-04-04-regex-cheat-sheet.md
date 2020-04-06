---
layout: post
date: 2020-04-04
title: "Regex cheat sheet for python"
---

I am writing a program that will find all the sex and sires in a raw data file and get rid of characters we don't need anymore.

## Character Classes

Character classes are a small group of characters that you need to use with an escape ```\```. They are used as a way of catching all the different types of a certain character.

For instance, instead of going ```[A-Za-z]``` you can just do ```\w``` and that will catch all the different word characters. There are a handful of them:

| Escape character | Use | Example |
| :------------- | :------------- | :------------- |
| ```\w``` | Word Characters | a-z, A-Z, 0-9, _ |
| ```\W```   | Non-Word Characters   | !@#$%^^&*()   |
| ```\d```   | Digits   | 0-9   |
| ```\D```   | Non Digits   | Not 0-9  |
| ```\s```  | White Spaces   | ```\t, \n, \r```   |
| ```\S```   | Non white spaces   | Opposite of above   |
| ```\b```   | Boundary of a word   | Basically the first or last letter of a word   |
| ```\b```   | Opposite   | Leaves off the first or last letter   |

The lowercase and upper case are the exact opposite. ```\d``` finds all digits (0-9) and ```\D``` finds the exact opposite.


## Special characters

Special characters are when things get helpful. I don't want to type out ```\w\w\w\w``` to find every 4 letter word. Seems silly.

| Special Character | Use | Example |
| :------------- | :------------- | :------------- |
| ```^``` | Beginning of a string | ```^\d``` |
|```$```   | Matches everything to it's left at the end of a string | ```\w$``` finds when I don't end a line with punctuation |
| ```.```   | Anything besides ```\n```   |   |
| ```\```   | Escape character   |   |
| ```|```   | OR   | ```A|B``` A OR B   |
| ```{N}```   | Number of times the thing to it's left needs to be found   | ```\w{4}``` Finds a word character 4 times in a row  |
| ```{N,}```   | Same as above, but N or more times   | ```\w{4,}``` Finds a word character 4 or more long  |
| ```{N,X}```   | Finds whatever code N through X times   | ```\w{4,6}``` Finds word characters that are 4 to 6 long   |
| ```*```   | Finds 0 or more times   | ```\w*``` Finds a word character 0 or more times   |
| ```+```   | Finds something 1 or more times.   | ```\d+``` Finds a digit 1 or more times   |
| ```?```   | Sort of optional. Like the () around the area code. Sometimes they're there other times they aren't   | ```\(?\d{3}\)?``` Finds the area code with optional ()   |


## Sets

Sets use brackets and are used for groups of characters. An example would be ```[A-Z]```. That would be every uppercase letter A-Z.

You also don't need to repeat letters so a letter can appear 1 or more times. For instance if I wanted to find "James Carney" it would look like this:

```
[jamescrny\s]
```

Carney looks a little weird because it has some letters that appear in James so they don't need to be repeated. I also added ```\s``` because there is a space between James and Carney.

| Set layout | Purpose |
| :------------- | :------------- |
| [ ] | Regular Set. Finds things between the brackets |
| [milk] | Finds either of those letters, but not all of them in one string |
| [a-z]   | Finds lowercase letters a-z   |
| [-a]   | Finds ```-``` and 'a' since the ```-``` is at the beginning of the set   |
| [^anything]   | the ```^``` excludes anything in the bracket   |
| []?*+   | Anything in the bracket, followed by the special character determines how many characters you're looking for   |
