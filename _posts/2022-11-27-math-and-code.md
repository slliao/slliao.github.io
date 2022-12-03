---
title: Math and Code
author: Mark
categories: [Tools, Markdown]
tags: [Markdown, LaTeX]
math: true
mermaid: true
pin: false
---

## Footnote

Click the hook will locate the footnote[^footnote], and here is another footnote[^fn-nth-2].

## Mathematics

The mathematics powered by [**MathJax**](https://www.mathjax.org/):

$$ \sum_{n=1}^\infty 1/n^2 = \frac{\pi^2}{6} $$

When $a \ne 0$, there are two solutions to $ax^2 + bx + c = 0$ and they are

$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$

## Inline code

This is an example of `Inline Code`.


## Code block

### Common
```
This is a common code snippet, without syntax highlight and line number.
```
### Specific Languages
#### Console
```console
$ env |grep SHELL
SHELL=/usr/local/bin/bash
PYENV_SHELL=bash
```
#### Shell
```bash
if [ $? -ne 0 ]; then
    echo "The command was not successful.";
    #do the needful / exit
fi;
```
## Reverse Footnote
[^footnote]: The footnote source
[^fn-nth-2]: The 2nd footnote source
