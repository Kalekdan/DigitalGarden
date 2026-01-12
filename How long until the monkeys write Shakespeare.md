---
title: How long until the monkeys write Shakespeare?
tags:
  - technology
maturity: seed
plantedDate: 2026-01-08
tendedDate: 2026-01-08
---
![[Pasted image 20260112104233.png]]
There's the classic thought experiment - if you had a room full of monkeys randomly typing away on keyboards, they'd eventually produce the entire works of Shakespeare. Now this is a mathematical certainty given infinite monkeys and inifinte time (or in fact 1 monkey and infinite time or inifinite monkeys and 1(?) time). But how long would it actually take. It seems like something you should be able to calculate, so I thought I'd give it a quick go with my limited probability knowledge. And maybe have a go at implementing a quick experiment to see how close I am.

### The Theory
We're going to work on the assumption that the monkey is hitting the keyboard totally randomly, it should be quite straightforward to work out how long it will take to type any given word. I'm also going to ignore spaces for now, as that adds another level of complexity we will talk about later.

Each letter has a 1/26 chance of appearing, so the chance of a 1 letter word being typed is 1/26. This very quickly becomes less and less likely the longer the input string is. A 2 letter word is 1/26 x 1/26, or 1/676. We can formalise this as 1/(26^n), where n is the length of string we're looking for (i.e. the length of the complete works of Shakespeare.)

### The Practice
Lets start easy, and only go up to a 6 letter word. From what we know we can predict how many letters we'd need to type to get the word to appear. I wrote a short script to programatically be my monkey and type random letters. Below are the results

| Input Length | Expected Random Letters Needed | Actual Random Letters Needed (first) | Actual Random Letters Needed (avg) |
|--------------|--------------------------------|--------------------------------------|------------------------------------|
| 1            | 26                             | 39                                   |                                    |
| 2            | 676                            | 1030                                 |                                    |
| 3            | 17576                          | 16691                                |                                    |
| 4            | 456976                         | 82483                                |                                    |
| 5            | 11881376                       | 308341                               |                                    |
| 6            | 308915776                      | 39865835                             |                                    |
