# Best practices for Data Scientists using Python

## Background

* All the participants are Data Science people with Msc or Phd
* Principles of correct and performant coding.
* Design Patterns.
* Clean code.
* Effective code.
* Object oriented vs functional.
* Profiling and optimization of numpy and pandas code.
* Code-review BKMs.


## Questions

* Are the people using git or some other vesrion control system? How familiar are they with it?
* Are people writing Jupyer notebooks only or are they writing libraries as well?
* Which libraries do they use besided numpy and pandas?

## Notes


* Are the people using git or some other vesrion control system? How familiar are they with it?
* Are people writing Jupyer notebooks only or are they writing libraries as well?
* What is considered "production" for them?
* What is the outcome of their work? Working code? A graph?
* How important is making the analyzis repeatable? On the same dataset. On another dataset?

* Code layout - black
* Linters: flake, pylint?
* Testing: verify the results of simple computations.
* Fixing the seed
* Checking that the results of computations (predictions) don't get worse, are within certain metrics.

* Which libraries do they use besided numpy and pandas?
* Do they have requirements.txt file or other way to specify the list of libraries they use?
* Do they use virtualenv or some other tool to separate environments?


## Object Or


### Code review

* It is really difficult, in most places I saw the code-reviews were not that useful
For small, almost trivial changes the need for code-review hindred the progress. (because the system required code-review for every change even typo fixes had to go through the process and when the people who were supposed to do the code-review were at lunch the others could not make progress)
For big changes, the reviewer it is usually quite difficult to understand the main issues of the code. So people tend to comment on trivial issues.

A better approach might be pair-programming. Working together on the same computer at the same time.



