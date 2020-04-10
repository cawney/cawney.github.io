---
layout: post
date: 2020-04-09
title: "Vim Cheat Sheet"
---


# Vim Cheats

These are a handful of helpful cheats I've learned along the way from going through Zed Shaw's ```Learn Code the Hard Way``` stuff. This is from the Vim course he has on the website. Just a small list of cheats that have helped me navigate Vim a little better than before.

## Motion

* G == go to line
* `` == go back to where I was
* f == find char back
* F == find char forward
* $ end of line, ^ beginning of line
* / search for thing
* ? backward search for thing
* n go to next search result
* m for mark. ma == mark a, mb == mark b. `a == go to mark a

## Change

* i -- inserting
* c -- change a thing, cw or any motion
* A -- append to the end of line
* I -- insert at beginning
* d -- delete, and can combine with any motion (dw, d$)

## Search

* / -- find a regex
* n -- next search

## Buffers

* :b file -- tab through files by chars in them
* ctrl-w -- slitting windows
    * s -- split horizontally
    * v -- split vertically
    * arrows -- go left, right, etc.
    * c -- close it

## Saving

* :wa -- save everything


## Repitition by count

Add count (number) followed by command
* 5w goes forward 5 words

* . -- do that thing again
* 10 -- do this next thing 10 times (5dw, delete the next 5 words)

## Recovery

* u -- undo
* :earlier TIME -- go back in time
* :later TIME -- go forward in time
