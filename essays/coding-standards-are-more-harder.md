---
layout: essay
type: essay
title: Coding Standards Are More Harder
date: 2017-09-21
labels:
- Reflection
- Software Engineering
- Coding Standards
---

<center><figure>
<img
src="https://i.imgur.com/7bf2N5X.png"
alt="If you use grammar incorrectly on the Internet, your gonna have a bad time.">
<figcaption>"Grammar, like coding standards, is a complex topic."</figcaption>
</figure> </center>

## This page's title is grammatically incorrect

Do you think the title of this web page makes the article seem unprofessional?
Unpolished? *Offensive?* *Dangerous?*

I think that the title is a good starting point as a analogy for coding
conventions -- sometimes, grammar is a trivial thing, and other times,
it can get in the way of things and make things harder to understand.

Enter: **coding standards**.

## Coding what?

**[Coding conventions](https://en.wikipedia.org/wiki/Coding_conventions)** or
*coding standards* are "a set of guidelines for a specific programming langauge
that recommend programming style, practices, and methods for each aspect of a
program written in that language."

## The trivial 
Coding standards sometimes refer to trivial topics, such as the variable
naming convention (`snake_case` or `camelCase` or `kebab-case`?). I find that
these topics can be compared to stuff like the usage of **whom** in English
-- they can be nice, but sometimes ineffectively pedantic.

Usually, coding standards are put into place for readability. And that's good.

## ESLint + IntelliJ

So, over the past week, I got the chance to setup IntelliJ for JavaScript
development with ESLint. And, due to my current ICS 314 class (Software
Engineering I) at University of Hawaii at Manoa, I've also adopted the
AirBNB coding standards for JavaScript in ESLint.

To be honest, I haven't really noticed it that much. Since I usually try to
use a coding formatter and thus a uniform coding style on my other projects,
I don't find too much resistance using ESLint.

## The next level stuff

In my opinion, coding standards are just the beginning on a long road to
maintainability and understandability of a code base. While things like
`gofmt` for the Go programming langauge and `clang-format` for C and C++
are nice for general code styles, it's doesn't do any big picture things
for helping people understand the "big picture" of code.

Take, for example, something like a C call graph:

<center><figure>
<a href="https://fossies.org/dox/cflow-1.5/gnu_8c.html">
<img
src="https://fossies.org/dox/cflow-1.5/gnu_8c__incl.png"
class="ui large middle image"
alt="A picture of a C dependency graph for a C application."
align="middle">
</a>
<figcaption>"An example of a C dependency graph generated by GNU cflow."</figcaption>
</figure> </center>

[GNU cflow](https://fossies.org/dox/cflow-1.5/gnu_8c.html) is an example of a
program that can generate more "high-level" representaton of a code base
to express the relationships of the concepts within it. Here, within the picture,
we see an example of how `src/gnu.c` may include `gettext.h` which may include
`stdlib.h`. This is a much better tool for maintainability of code than
simpler things like code style as enforced by a code linter.

In my opinion, the power of linters and simple stylers is limited. This is
because the more important concepts of design and semantic coding standards
are often not able to be enforced by more simple tools; and, these tools are
also not taught within the classroom. This is because tools to enforce what
dependencies to use are often domain-specific or handled by niche tools
(e.g. I encountered a similar tool to track dependency usage and recommend
better versions when interning at a company).

Some languages have better support for doing these types of things -- for
example, Java contains the `@Deprecated` annotation that can mark
methods as "deprecated" and produce compiler warnings if one tries to use
a deprecated method. This is an example of something that can help enforce
semantic coding standards (e.g. don't use `scanf()`).

## The limits of restriction

Right now, it feels like beginners do not learn how to limit their own
coding conventions and semantic conventions, similar to how people may
have different ways of note-taking and listening in real life. Ultimately,
the **semantic** concepts of using certain idiomatic patterns, feature, or
libraries is what ultimately matters when learning a language, as these
represent wisdom on how to structure programs to make them understandable
to others, as well as to (usually) make them more clear or efficient.

A language that had a great amount of power in controlling this would be
a great language to use to teach people the power of coding conventions
and standards.

## Self control

Extending this idea -- I think people learn best when they learn how to
learn independently and control their own learning.

A beginner that could control their own coding conventions and semantic
conventions would ultimately be a beginner that could start to learn
in a more structured and efficient manner, guided by the conventions of
those with more experience.

## The bottom line

The bottom line: good conventions are good because they facilitate
instinct for better decisions and designs. One learns better when these
conventions can be enforced so that beginners can learn what is right
and what is wrong for a given domain or language.


