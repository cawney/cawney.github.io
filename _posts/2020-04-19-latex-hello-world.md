---
date: 2020-04-19
layout: post
name: "LaTex Hello World"
---

I've been working on something I think will be interesting. It's a layout of California Chrome's family tree with notable ancestors highlighted. I'm using a program called `LaTex` to do it. It's a type setting program used mostly in the academic world, but it has uses everywhere. I'm writing this to give a basic `Hello, world` sort of document.

## Beginning the document

The first thing you need is a document class. There are a ton to choose from. Article seems to be a great starting point. You can find a big list of them [here](https://ctan.org/topic/class).

To start the document, it should look like this:

```latex
\documentclass{article}
```

That should be the beginning of the file. Now you need to tell it to build the actual document. To do that, need to add the begin tag with what you're beginning. It should look like this:

```latex
\begin{document}
```

Then put in the text like you would in any text editor:

```latex
Hello world
```

Then you need to end your document, it will use the end tag with document. Like this:

```latex
\end{document}
```

## All together

What it looks like all together:

```latex
\documentclass{article}
\begin{document}
Hello world
\end{document}
```

## Compiling

If you give someone a document that looks like the one above with the slashes and the curly brackets, they'll have no idea what it's supposed to look like. You need to use the LaTex compiling tools to turn it into something readable.

I found the easiest way to make a PDF was to download latexmk. It's a perl script that makes a bunch of fancy things automatically. After downloading, run this:

```
latexmk -pdf document.tex
```

And that should a lot of files, including your PDF. There's also a program called pdflatex, but I've gotten several errors while using it, and haven't with latexmk. I'll play with it a bit more, because the obvious choice for me is just pdflatex since it just makes a pdf and not all the extra files that I have no need for.
