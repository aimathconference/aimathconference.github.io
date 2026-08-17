---
layout: page
title: Resources
---

The following resources are provided in order to help participants get the most out of this workshop.
There is a lot of material here, and you may not be able to get through everything by the time of the workshop.
Our goal is to give you more than what is necessary, with the expectation that learning *anything* here will be beneficial.

### **Environment Resources**

These resources are intended to help you get familiar with a development environment. Most (if not all) of these resources are designed for a Unix-based operating system (e.g. Linux or macOS). If you are using a machine with a Windows-based operating system, we recommend you install and use the Windows Subsystem for Linux (WSL); see [here](https://learn.microsoft.com/en-us/windows/wsl/install) for information on how to set this up.

A comprehensive course for this material is provided by the MIT Computer Science & Artificial Intelligence Laboratory (CSAIL) course ["The Missing Semester of Your CS Education"](https://missing.csail.mit.edu/).
Additional resources are provided below; some of these contain more, or more elementary, information than MIT's CSAIL course.

**[Using a Unix Terminal/Shell](https://info-ee.surrey.ac.uk/Teaching/Unix/)** - The terminal is a text interface for running commands and programs on your machine. Using a keyboard/text-driven terminal (as opposed to a mouse-driven graphical interface) gives you finer control over the commands you want your machine to execute and allows for greater composability between programs.

**[Using Git](https://marklodato.github.io/visual-git-guide/index-en.html?no-svg)** - Git is a program for managing the version control of a project. You can think about a project as a directed acyclic graph: the first node in this graph is the start of a project; as you edit files and directories in a project, eventually you want to make a new checkpoint (or version) of your work (maybe you've added a feature, or fixed a bug) -- with Git, you can `commit` this version as a new node in the graph pointing to the node it is built from (dependent on); Git gives you tools to build from various nodes of the graph, and to create a new `branch` when you do so; and if someone else wants to build on your project, they can copy all of its files and its graph (`clone`), and start working on an independent copy on their machine. Eventually, you may want to combine versions between different groups, and Git provides tools for doing this as well (`merge`, `rebase`, etc.).

**Text Editors** -
We recommend that you choose a text editor for making changes to your files and programs. 
Your terminal is likely already equipped with a simple text editor like [nano](https://www.nano-editor.org/) or [Vim](https://www.vim.org/). 
The most popular alternative text editor is Microsoft's [Visual Studio Code](https://code.visualstudio.com/); it is very well-developed, the source code is free (as in "freedom"), but the binary distributed on the official website is free (as in "free beer") and captures telemetry data by default.
You might also be interested in options like [Emacs](https://www.gnu.org/savannah-checkouts/gnu/emacs/emacs.html) or [Neovim](https://neovim.io/), which have binaries that are free (as in "freedom"), are open-source and do not capture telemetry data, but are typically viewed as more advanced tools when it comes to configuration.

### **Programming Resources**

There are a plethora of programming languages available today (e.g. C, C++, C#, D, Ruby, Java, Python, Perl, Lisp, Julia, [etc.](https://en.wikipedia.org/wiki/List_of_programming_languages)).
A programming language provides a set of commands that you can use to coordinate the hardware of a machine to accomplish a desired task.
Programming languages can have varying levels of abstraction (in this context, abstraction is roughly a measure of how far a command is from direct instructions on the hardware).
We will primarily use, in the examples below, Python, Julia, or Lean; these languages are considered high-level with a lot of abstraction.


**[An introduction to Python](https://github.com/benedictpaten/intro_python)** - Python is the most popular programming language for AI use. It's a versatile programming language, which allows for coding many different types of applications. It's also relatively easy to get started with programming in Python; the associated link goes to slides for the first-year course, "CSE 20: Beginning Programming in Python" at UC Santa Cruz. 
These lectures consist of interactive Jupyter notebooks, which are a convenient way to write and execute Python code.

**[An introduction to Julia](https://benlauwens.github.io/ThinkJulia.jl/latest/book.html)** - Julia is, in comparison to Python, a niche programming language.
Its primary advantage compared to Python is that it is a just-in-time (JIT) compiled language; this means that code is compiled when it is run for the first time (in a script, for example), which allows subsequent calls to run much faster.
It is also the language that [OSCAR](https://www.oscar-system.org/) (the Open Source Computer Algebra Research system) is built on top of.

**[An introduction to Lean](https://lean-lang.org/functional_programming_in_lean/)** - Unlike both Python and Julia, which are imperative languages (meaning, roughly, that code consists of statements that execute line-by-line from the top down), Lean is a functional programming language. 
More commonly, Lean may refer to the formal interactive proof assistant, which is made possible by the typechecker of the Lean programming language.
To get started with mathematical formalization with Lean, [look here instead](https://leanprover-community.github.io/mathematics_in_lean/).

**Writing and Executing Code** - There are a number of different ways to write and to execute code.
Simple Python or Julia code can be evaluated in a **R**ead **E**valuate **P**rint **L**oop (or REPL). 
You can start the REPL for either language by typing `python` or `julia` in a terminal.
Python or Julia code can also be executed in the terminal as a script (i.e. a file `hello_world.py` can be run from the shell with `python hello_world.py`).

Python and Julia are also both supported by runtimes in Jupyter Notebooks.
There are many ways to run a Jupyter Notebook (e.g. you can run them locally with [Jupyter](https://jupyter.org/); 
Google also provides the free-to-use [Google Colab](https://colab.research.google.com/) platform for remote code execution).
The benefits of using a Jupyter Notebook include: an environment
for reading rich text detail (e.g. mathematical symbols rendered with LaTeX) alongside code, a simple code execution environment, and statefulness (it remembers past computations or code executions). 
You may find it more appealing to use a Jupyter Notebook for some tasks.

### **LLM Resources**

[Calling an API/Writing a loop]()
