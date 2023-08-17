# Best practices for Data Scientists using Python

## Background

* All the participants are Data Science people with Msc or Phd.
* Principles of correct and performant coding.
* Design Patterns.
* Clean code.
* Effective code.
* Object oriented vs functional.
* Profiling and optimization of numpy and pandas code.
* Code-review BKMs.


## Notes

* Are the people using git or some other version control system? How familiar are they with it? - Yes, very familiar.
* Are people writing Jupyer notebooks only or are they writing libraries as well? -  Both. Mostly using PyCharm.
* How many years of experience writing Python code do they have? - Varying between 2 and 20, mostly targeting the 3-5 years audience
* Who initiated the idea of this course? The people who will participate? Their manager? What is the main problem they face? - Good design and better optimization are the main needs. Raised both in a survey and by managers.

* What is considered "production" for them?
* What is the outcome of their work? Working code? A graph?
* How important is making the analyzis repeatable? On the same dataset. On another dataset?

* Code layout - black
* Linters: flake, pylint?
* Checking that the results of computations (predictions) don't get worse, are within certain metrics.

* Which libraries do they use besides numpy and pandas? - Scikit-learn, tensorflow, pytorch, huggingface.
* Do they have requirements.txt file or other way to specify the list of libraries they use?
* Do they use virtualenv or some other tool to separate environments?


* [Agile Manifesto](https://agilemanifesto.org/)
    * There is no single best way to do things. We are constantly trying to improve ourselves and our code.
* Most of the time we spend on reading and trying to understand code, rather than writing code.


## Effective code.

* Testing: verify the results of the computations.
* Verify the result of algorithms with random elements. Fixing the seed.



## Clean code

* DRY
* meaningful variable names
* short functions that do only one thing
* refactoring

* Make people re-read their own code a few months after they wrote it and let them refactor it!
* Frequently switch people between projects so they will need to read and understand each others code.
* Book: "Clean Code: A Handbook of Agile Software Craftsmanship by Robert C. Martin"
* [Clean Code Explained](https://www.freecodecamp.org/news/clean-coding-for-beginners/)
* [How to Write Clean Code – Tips and Best Practices](https://www.freecodecamp.org/news/how-to-write-clean-code/)


## Performance - Efficient code.

* Profiling
    * [ydata-profiling](https://github.com/ydataai/ydata-profiling)
    * [py-spy](https://pypi.org/project/py-spy/)
* Benchmarking
* Rewrite computation heavy parts in C, C++, or Rust.
* Levenshtein disatance
    * https://pypi.org/project/python-Levenshtein/
    * https://pypi.org/project/Levenshtein/
    * https://pypi.org/project/editdistpy/
* Parallel programming (multiprocess)
* Caching
* Using the memory instead of the disk.
* [Algorithmic Time complexity](https://en.wikipedia.org/wiki/Time_complexity) of the algorithm used.
* Using dict instead of list.

* [using numba](http://numba.pydata.org/)
* [Nuitka](https://nuitka.net/) - the Python Compiler

* [Scipy Optimizing code](https://scipy-lectures.org/advanced/optimizing/)

## Object Oriented vs Functional programming

* lazy evaluation
* working with long, possibly infinite series of numbers


### Code review

* It is really difficult, in most places I saw the code-reviews were not that useful
For small, almost trivial changes the need for code-review hindred the progress. (because the system required code-review for every change even typo fixes had to go through the process and when the people who were supposed to do the code-review were at lunch the others could not make progress)
For big changes, the reviewer it is usually quite difficult to understand the main issues of the code. So people tend to comment on trivial issues.

A better approach might be pair-programming. Working together on the same computer at the same time.



