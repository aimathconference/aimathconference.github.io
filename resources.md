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
You might also be interested in options like [Emacs](https://www.gnu.org/software/emacs/) or [Neovim](https://neovim.io/), which have binaries that are free (as in "freedom"), are open-source and do not capture telemetry data, but are typically viewed as more advanced tools when it comes to configuration.

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

These resources are intended to provide you with a variety of ways for how you can use an LLM (outside of the
standard chat-interface subscription-based model available through consumer plans at Anthropic, Google, or OpenAI).

Without going into any significant detail, an LLM (**L**arge **L**anguage **M**odel) is a function that takes in a prompt and outputs some text.
Models can be differentiated by their *architecture* (the concrete implementation of this function) and their *weights* (specific values reached through training that influence how the LLM behaves on a given input).
There are a variety of models accessible to you right now (including open-source and open-weight models). Many are hosted and available to download from the [Hugging Face](https://huggingface.co/) website. 

**Models** - We point out a couple of examples: [Qwen3.8-27B](https://huggingface.co/Qwen/Qwen3.8-27B), [MiniCPM5-2B](https://huggingface.co/openbmb/MiniCPM5-2B), [GLM-5.3](https://huggingface.co/zai-org/GLM-5.3). Note that models typically display their parameter count (e.g. the 27B in Qwen3.8-27B, or the 2B in MiniCPM5-2B). This number can be used to get a rough estimate on the size of the model: one byte is eight bits; 
one parameter can be represented as a 16-bit floating point number (FP16 or BF16), an 8-bit floating point number (FP8), in a 4-bit format (INT4 or FP4), or even as a single bit (as well as a number of other formats); a model using 27 billion parameters (27B) at FP4 precision then takes up about 13.5(= 27 * 4 / 8) billion bytes of space, i.e. 13.5 Gigabytes (GB). Most models are loaded fully into memory (e.g. RAM, VRAM, unified memory, or a mix) when they are ran; this is one constraint on which models you'll be able to run on a given piece of hardware (e.g. Qwen3.8-27B can run on many consumer GPUs using FP4 precision or similar, MiniCPM5-2B can run on many consumer laptops at almost all precisions, and you probably can not run the 753B GLM-5.3 model at any precision without a very sophisticated set-up). 
Other, second-order features will also impact the amount of memory a model needs (e.g. an LLM needs a KV cache, whose size is related to how the model is served and how much context --- roughly the number of tokens a model can cumulatively input and output in one turn --- the model is allowed) so parameter count really is a rough *lower bound*.

Models can exist for different purposes (e.g. for parsing pdf files, for producing accurate Lean code, or for general-purpose user interactions).
It can be revealing, in some ways, to compare different models on different benchmarks; some prominent math related benchmarking can be found here:
[MathArena](https://matharena.ai/), [EpochAI](https://epoch.ai/frontiermath). 
To judge which model you would want to use, however, you'll likely need to test it yourself.

**Inference** - Inference is the process of an LLM producing output to a given prompt.
There are open-source projects that have been developed to make running LLMs, with varying architectures and weights, very manageable; the two that we can recommend are: [vLLM](https://vllm.ai/) and [llama.cpp](https://llama.app/). 
Both vLLM and llama.cpp provide an *inference engine*, the program responsible for running a given model. 
They also provide a number of different points of access to this engine, for example a CLI (command line interface) and an HTTP server with an OpenAI-compatible API.
This means that you can, for example, enter a prompt directly into the CLI and get a response in your terminal; you can host a model locally and allow anyone on your local network to connect to (and use) the server; or you can write a script that uses an API endpoint, and freely swap the endpoint to other cloud providers as your needs demand.

**Hosting** - When a program runs an LLM, it acts as a *server*; a *client* is a process that wants something from the server (in analogy with how a restaurant might function). Where will the LLM that you want to use run? Will the server be hosted locally (on your local machine) or remotely (on a machine somewhere else, that you possibly do not own)? Everyone can run an LLM hosted locally on their own machine (e.g. MiniCPM5-2B using llama.cpp), but your mileage will vary greatly depending on your hardware.

If you don't have hardware that is sufficient for your needs, you can try running inference on a GPU that is provided by a cloud service. [Google Colab](https://colab.research.google.com/) is a web-based platform for using Jupyter Notebooks; Colab provides free access to an Nvidia Tesla T4 GPU with 16 GB of VRAM, with some restrictions on availability and usage, and paid access to higher end GPUs with less restrictions. 
If you are a researcher at a US university or nonprofit, you may qualify for access to an LLM namespace with the [National Research Platform](https://nrp.ai/), which can provide you with an API endpoint for use in your research.

**Examples** - The following examples are Jupyter notebooks designed to (minimally) show you that interacting with an LLM programmatically has enormous potential beyond what you might expect if you've only used a chat-based LLM before.
- First, here is a notebook for [calling an API](/assets/jupyter/intro_llm_api_key.ipynb){: download} to perform inference with an API key. 
- Here is a notebook for a simple [iterative proof development system](/assets/jupyter/iterative_proof_system.ipynb){: download}, which relies on calling an LLM via an API inside a `for` loop. 
- Here is a notebook for [improving the efficiency of a computational algorithm](/assets/jupyter/iterative_algorithm_optimization.ipynb){: download} in a similar vein.

**(Agentic) Harnesses** - An LLM, called from the inside of a while loop, has the option to request information which it can add to its context to help it respond to a given prompt on the next iteration of the loop; this gives the LLM some amount of *agency*.
A **harness** is an additional program that wraps LLM inference in order to add to the abilities and capabilities of the LLM.
A harness may be equipped with a collection of tools that the LLM can use in order to achieve its results; these tools may be passed to the LLM concatenated to an initial prompt and, based on the response of the LLM, called by the harness before returning to the LLM or the user (e.g. "You also have the option to use 

```json
  {
    "tool": "bash",
    "script": "enter your script here" 
  }
```
respond in this format if you want to use this tool"). A harness may also provide quality of life improvements to LLM use (e.g. the ability to summarize long LLM responses, and to continue from the summary, if the LLM goes beyond its context limit).

There are a number of sophisticated harnesses already developed and ready-to-use in your work. LLM and inference providers often develop a harness that can be used with their models (e.g. OpenAI has developed Codex as a harness that you can use with its models, and Anthropic has Claude Code for theirs). There are open-source options as well: [OpenClaw](https://openclaw.ai/) is an agentic harness that popularized the transition to agents; [Hermes](https://hermes-agent.nousresearch.com/) is an agentic harness that saves skills with use; [Pi](https://pi.dev/) is a minimal harness with the ability to read, write, edit, and "bash". A major differentiator between each of these harnesses are their philosophy for use: OpenClaw is very much a complete harness out-of-the-box; Hermes advocates for using their harness as a worker that you can even text commands to; Pi is very bare bones, and advocates for editing the harness itself (just ask your agent to do it) when you want to add a tool, or change a feature.

Using a harness comes with some innate risks (e.g. will the LLM make a tool call to the internet, and be prompt injected by a malicious actor? will it delete all of your files by accident?). However, modern LLMs trained for agentic work are often very capable. You will likely see major productivity gains from using a harness, and we recommend considering the option carefully.
