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

* Which libraries do they use besides numpy and pandas? - [Scikit-learn](https://scikit-learn.org/), [tensorflow](https://www.tensorflow.org/), [pytorch](https://pytorch.org/), [huggingface](https://huggingface.co/).
* Do they have requirements.txt file or other way to specify the list of libraries they use?
* Do they use virtualenv or some other tool to separate environments?


* [Agile Manifesto](https://agilemanifesto.org/)
    * There is no single best way to do things. We are constantly trying to improve ourselves and our code.
* Most of the time we spend on reading and trying to understand code, rather than writing code.


## Effective code.

* Testing: verify the results of the computations.
* Verify the result of algorithms with random elements. Fixing the seed.

## Version Control system

* Small commits
* Good commit messages


## Clean code

* DRY
* meaningful variable and function names
* short functions that do only one thing
* As much as possible make the code in a way that includes the story instead of commenting.
* Comment where necessary (explain why you made a certain decision in the code)
* refactoring, that implies automated unit and integration testing
* Remove old code (don't leave commented out old code around, you have version control if you need to go back and look at it again)

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
* Levenshtein distance
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

### Scikit-Learn

* [Scikit-Learn optimize for speed](https://scikit-learn.org/stable/developers/performance.html)

### Tensorflow

* [Optimize Tesnorflow performance using the Profiler](https://www.tensorflow.org/guide/profiler)
* [Optimize TensorFlow GPU performance with the TensorFlow Profiler](https://www.tensorflow.org/guide/gpu_performance_analysis)
* [Tensorflow performance best practices](https://www.tensorflow.org/lite/performance/best_practices)

### PyTorch

* [Profiling your PyTorch Module](https://pytorch.org/tutorials/beginner/profiler.html)
* [torch.profiler](https://pytorch.org/docs/stable/profiler.html)


## Object Oriented vs Functional programming

* lazy evaluation
* working with long, possibly infinite series of numbers


### Code review

* It is really difficult, in most places I saw the code-reviews were not that useful
For small, almost trivial changes the need for code-review hindered the progress. (because the system required code-review for every change even typo fixes had to go through the process and when the people who were supposed to do the code-review were at lunch the others could not make progress)
For big changes, the reviewer it is usually quite difficult to understand the main issues of the code. So people tend to comment on trivial issues.

A better approach might be pair-programming. Working together on the same computer at the same time.

## Notes

* Background not computer science
* They might have done OOP course and might use OOP but they might not know the architecture and the design patterns.
* Not always ideal about run time performance.

1. Better design of software
2. Better performance

* Functional programming

* Problems with class design.
* There is no "right way", but one way might be better than the other.
* When to use module instead of class. singleton - explain


## Plan for a 1 day course

* 9:00-17:00 we have 6 hours of training + 1 hour lunch break + 4*15 break.

### Goal:

* How to create better designed software that has better performance and it is easier to maintain?

### Topics

* Quick overview about algorithmic complexity. Big O notation. (1 hour)
    * Linear scan of data vs binary search in ordered data. (eg. git bisect)
    * List vs. Dictionary. (hashing) (eg. counting words)
    * Well designed lookup table in the memory. (e.g. [Counting Amino Acids](https://code-maven.com/slides/python/exercise-count-amino-acids))

* Parallel programming (1-2 hours)
    * Show [multiprocessing](https://code-maven.com/slides/python/multiprocess)

* Shorten the feedback loop: (20-30 min)
    * Clients
    * QA
    * CI with automated tests
    * Code review
    * Pair programming

* Refactoring - the secret is writing automated tests. (1-2 hours)
    * Show test coverage data of open source projects.
    * Show how to write a simple test for simple code.
    * Show how to write test for code that depends on randomization.

* OOP design patterns (1-2 hours)
    * General concept of design patterns as a way to talk about designs
    * Singleton
    * The overuse of inheritance. (A class to represent things with legs.)
    * Composition over inheritance
    * Dependency injections
    * Decorators
    * Encourage to review more design patterns.
    * [Python Patterns](https://python-patterns.guide/)
    * [Design Patterns in Python](https://refactoring.guru/design-patterns/python)

* Introduction to functional programming paradigm (1-2 hours)
    * range, map, filter, list comprehension, generator expression, lazy evaluation.
    * Part of [these slides](https://code-maven.com/slides/python/functional)


