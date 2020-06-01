---
date: 2020-05-16
title: "Command Line Mastery"
layout: post
category: [Command Line, Master the Craft]
author: "James Carney"
---

The command line is supposed to be much faster than using a GUI interface. From what I've read, the command line's speed to do things is it's biggest advantage over the GUI interface we all know and love. My biggest problem is I don't know the commands to make it quicker. I can navigate to a spot on my  computer pretty quickly using command line, but I don't really know any shortcuts other than that.

Well, I know the shortcuts, but I don't *know* the shortcuts. I can't type them out like they are an extension of me. I have the think hard about what I want to do, then I'll manage to remember. That is my biggest issue. I don't intuitively know what to do when I get to a spot on my computer via command line. The books I've read ([Pragmatic Programer](http://pragprog.com)) has talked about how the command line is to a programmer as a workbench is to a carpenter. It's a tool that serves little purpose to someone who isn't an expert in their craft, but if they know how to use it properly, they can work wonders around the layman.

I'm the layman. I'd classify myself as a hobby programmer. I know enough to get annoyed by how hard programming is. So my first job I'm trying to tackle is learning as much as I can about command line so I can at least use the workbench. If I can get really good at this, then that's one less thing I'll have to worry about when I'm trying to learn.

## Navigation

The basics of navigating your command line are (you guessed it), pretty basic:

| Command | Purpose |
| --- | --- |
| cd | Change directory |
| pwd | Print working directory |
| cd ~ | Change to home directory |
| ls | List what's in current directory |

When moving around, cd is how you do that. So if you want to get to your Documents folder and you're in your home directory, you'd type `cd Documents`. If you're in your home directory and you wanted to get to your folder called dogs what's inside your documents folder, you'd type `cd Documents/dogs`. It's pretty straight forward.

The `pwd` is helpful when you get lost and aren't sure where you are. If you type that in it will tell you what folder and where it is in relation to the home or root directory. It's pretty handy stuff.

## Managing files

Managing files is the main thing you do on a computer. You update, delete and add files to a computer every time you work on one. Doing this on the command line can save you time. The main commands are as follows:

| Command | Purpose |
| --- | --- |
| rm | Remove/Deletes a file |
| cp | Copy and pastes a file.[^1] |
| mv | Cut and pastes a file.[^2] |

[^1]: `cp this.md tohere.md`
[^2]: `mv thisisgone.md thiswasthat.md`
