# setup-example

[![python](https://img.shields.io/badge/python-3.9-blue.svg)](https://www.python.org/)
![os](https://img.shields.io/badge/os-ubuntu%20|%20macos%20|%20windows-blue.svg)
[![license](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/sandialabs/sibl#license)

[![tests](https://github.com/Lejeune-Lab-Graduate-Course-Materials/setup-example/workflows/tests/badge.svg)](https://github.com/Lejeune-Lab-Graduate-Course-Materials/setup-example/actions) [![codecov](https://codecov.io/gh/Lejeune-Lab-Graduate-Course-Materials/setup-example/graph/badge.svg?token=4KGN3VRWZ4)](https://codecov.io/gh/Lejeune-Lab-Graduate-Course-Materials/setup-example)

The purpose of this repository is to document an outline of the steps that go into setting up a very basic software development environment. This specific configuration is not mandatory for the ME 500 class, but we believe that the strategies suggested here will be helpful and useful. In some places, I have used [ChatGPT](https://chatgpt.com/) to make creating this readme file easier. Any text primarily written by ChatGPT is reported in *italic font* (in some cases I have made edits and/or added additional information). I have independently verified all text generated by ChatGPT and take responsibility for its content. For each general concept, I encourage you to learn more on your own as is helpful to your understanding. The first assignment for this class will involve learning by doing.

### Table of Contents

* [General Philosophy](#phil)
* [Command Line](#cmd)
* [Python](#python)
* [GitHub](#github)
* [Anaconda](#anaconda)
* [Visual Studio Code](#vscode)
* [Test Driven Development via pytest](#tdd)
* [Code Coverage via codecov and GitHub Actions](#codecov)
* [Markdown](#markdown)
* [Code Review](#review)
* [Generative AI Policy](#genAI)
* [Instructions for This Repository](#instructions)

### General Philosophy <a name="phil"></a>

One of the goals of this course is to increase comfort with open source software (both as a user and as a potential contributor). When using open source software, it's important to learn how to figure things out as you go along, and not overly rely on being able to follow a step by step tutorial for everything that you need to do (though well done tutorials are fantastic!). When something doesn't work as initially planned, there are several different strategies that you can use to figure out what to do next (e.g., take some time to think about the problem, try and break the problem down into smaller more manageable pieces, search online for an answer, post on a forum etc.). The best next step will depend on the problem, and figuring out how to navigate this is part of the process. To this end, please view this setup guide as a resource page rather than a specific list of instructions. It will require some non-trivial amount of effort to get comfortable with all of these tools -- that is normal!

### Command Line <a name="cmd"></a>
```
how do you concisely define the terminal (computer programming)?
```

ChatGPT:

*In computer programming, a terminal is a text-based interface that allows users to interact with a computer's operating system by entering and executing commands, typically through a command-line shell like Bash or Command Prompt. It is used for tasks such as running scripts, managing files, and controlling processes.*

```
how do you access the terminal on linux, max, and windows machines respectively?
```
ChatGPT:

*Linux: Most Linux distributions have a terminal pre-installed.
To open it, press Ctrl + Alt + T or search for "Terminal" in the application menu.*

*macOS: Open Spotlight Search (press Cmd + Space) and type "Terminal." Alternatively, go to Applications > Utilities > Terminal.*

*Windows: For the Command Prompt, press Win + R, type cmd, and press Enter. For PowerShell, press Win + X and choose Windows PowerShell or search for "PowerShell" in the Start menu. Alternatively, use Windows Terminal by searching "Windows Terminal" in the Start menu (available in recent versions). Please note that newest version of PowerShell might not be installed automatically on your machine and updating may be preferible.*

Overall, the best way to learn how to use the terminal is to just give it a try! The resources provided below include tutorials to get started on your own computer. Basic abilities in command line programming will be necesary for this course.

Additional resources:
* [BU RCS Introduction to Linux Tutorial Sign Up](https://www.bu.edu/tech/about/training/classroom/rcs-tutorials/)
* [BU RCS Introduction to Linux Tutorial Slides](https://www.bu.edu/tech/files/2019/01/2019-Spring-Tutorial-Introduction-to-Linux.pdf)
* [Example Linux Cheat Sheet](https://files.fosswire.com/2007/08/fwunixref.pdf)
* [Terminal Cheat Sheet](https://terminalcheatsheet.com/)

### Python <a name="python"></a>
The emphasis of this class will be on contributing to the open source software ecosystem and we will also plan to use the python based finite element analysis software FEniCS. Therefore, we will focus primarily on the python programming language.

```
what are the key features of the python programming language?
```
ChatGPT:

*The key features of the Python programming language are:*
1. *Simple and Easy-to-Learn Syntax: Python emphasizes readability, allowing developers to write clear and concise code.*
2. *Interpreted Language: Python code is executed line-by-line, making it easier to debug and run without a compilation step.*
3. *Dynamically Typed: Variables in Python are assigned types at runtime, meaning you don't need to declare types explicitly.*
4. *High-Level Language: Python handles low-level details like memory management, allowing developers to focus on solving problems.*
5. *Extensive Standard Library: Python has a large standard library that supports many common tasks like file handling, web development, and data manipulation.*
6. *Cross-Platform Compatibility: Python code can run on different operating systems (Windows, macOS, Linux) without modification.*
7. *Support for Multiple Programming Paradigms: Python supports object-oriented, procedural, and functional programming styles.*
8. *Third-Party Libraries and Frameworks: Python has a vast ecosystem with libraries for web development (Django, Flask), data science (NumPy, pandas), machine learning (TensorFlow, PyTorch), and more.*
9. *Community Support: Python has a large and active community, which contributes to its development and provides extensive resources for learning and troubleshooting.*
10. *Scalability and Extensibility: Python can integrate with other languages like C/C++ for performance-critical tasks and supports modules that extend its functionality.*

*These features make Python versatile and popular for a wide range of applications, from web development to scientific computing.*


Additional resources:
* [NumPy for MATLAB users](https://numpy.org/doc/stable/user/numpy-for-matlab-users.html)
* [A Python Primer for Matlab Users](https://bastibe.de/2013-01-20-a-python-primer-for-matlab-users.html)
* [BU RCS Python Tutorials Sign Up](https://www.bu.edu/tech/about/training/classroom/rcs-tutorials/)
* [Python For Beginners](https://www.python.org/about/gettingstarted/)

### GitHub <a name="github"></a>

```
what is GitHub useful for?
```

ChatGPT:

*GitHub is useful for a variety of purposes, especially in software development and collaboration. Its key uses include:*
1. *Version Control: GitHub helps track changes in code over time using Git, allowing developers to manage different versions of a project.*
2. *Collaboration: Multiple developers can work on the same project simultaneously, merge changes, and resolve conflicts through pull requests.*
3. *Backup and Storage: GitHub acts as a cloud-based repository to store and back up code and project files.*
4. *Open Source Contributions: It hosts many open-source projects, allowing developers to contribute to existing projects or share their own work.*
5. *Project Management: GitHub provides tools like issues, project boards, and milestones to manage tasks, bugs, and development workflows.*
6. *Code Review: Developers can review each other's code, comment, and suggest changes to ensure code quality.*
7. *Documentation: GitHub supports Markdown for writing project documentation, README files, and wikis.*
8. *Continuous Integration/Deployment (CI/CD): It integrates with CI/CD tools to automate testing, building, and deployment processes.*
9. *Community Building: GitHub fosters communities around projects by allowing users to star, fork, and watch repositories.*
10. *Portfolio Hosting: Developers use GitHub to showcase their projects and skills by sharing their work publicly.
GitHub is a powerful platform for code hosting, collaboration, and version management, widely used in both open-source and professional environments.*

Additional resources:
* [Install Git](https://github.com/git-guides/install-git)
* [GitHub Tutorial](https://docs.github.com/en/get-started/start-your-journey/hello-world)

### Anaconda <a name="anaconda"></a>

```
what is anaconda (python)?
```

ChatGPT:

*Anaconda is a popular open-source distribution of Python (and R) that simplifies package management and deployment. It is designed for data science, machine learning, and scientific computing. Key features of Anaconda include:*

1. *Pre-packaged Libraries: Anaconda comes with over 1,500 popular data science packages (like NumPy, pandas, scikit-learn, TensorFlow, etc.), making it easier to set up environments.*
2. *Conda Package Manager: Anaconda uses Conda, a package manager that helps install, update, and manage libraries and dependencies, including non-Python packages.*
Virtual Environment Management: Conda also allows you to create isolated virtual environments to manage different project dependencies separately.*
3. *Jupyter Notebooks: Anaconda includes Jupyter, a tool for creating and sharing documents that contain live code, visualizations, and narrative text.*
4. *Cross-Platform: Anaconda works on Windows, macOS, and Linux, providing consistency across different operating systems.*
5. *Anaconda Navigator: A GUI tool to manage packages, environments, and launch applications like Jupyter, Spyder, and RStudio without using the command line.*
6. *Enterprise Support: Anaconda offers enterprise solutions for managing large-scale data science workflows in teams and organizations.*

*Anaconda is widely used by data scientists, machine learning engineers, and researchers because it simplifies complex environment and dependency management.*

Additional resources:
* [Anaconda Installation](https://docs.anaconda.com/anaconda/install/)
* [Getting Started with Conda](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html)

### Visual Studio Code <a name="vscode"></a>

```
what is Visual Studio Code?
```

ChatGPT:

*Visual Studio Code (VS Code) is a lightweight, open-source code editor developed by Microsoft. It is widely used by developers for writing and debugging code in a variety of programming languages. Key features of VS Code include:*

1. *Code Editing: Provides a fast and flexible environment for editing code with syntax highlighting, auto-completion, and intelligent suggestions for many programming languages.*
2. *Integrated Development Environment (IDE) Features: Although lightweight, VS Code offers features like debugging, version control (Git integration), and terminal access, making it a powerful coding tool.*
3. *Cross-Platform: Works on Windows, macOS, and Linux, allowing a consistent development experience across operating systems.*
4. *Extensibility: Supports a vast marketplace of extensions, enabling users to add functionality like language support, themes, and tools for various frameworks (e.g., Python, JavaScript, Go, etc.).*
5. *Built-in Git Support: VS Code has built-in support for Git, allowing users to manage version control, stage commits, push changes, and review code directly from the editor.*
6. *Debugging Tools: Provides built-in debugging for various languages, with features like breakpoints, watch variables, and step-through debugging.*
7. *Integrated Terminal: Offers a built-in terminal that allows users to run shell commands and scripts directly inside the editor.*
8. *Snippets and IntelliSense: Includes code snippets for quicker development and IntelliSense, which provides smart code completions based on variable types, function definitions, and more.*
9. *Customizable: Developers can personalize their workspace by adjusting settings, themes, and keyboard shortcuts.*

*VS Code is widely popular because it balances the simplicity of a code editor with the powerful features of a full IDE, making it suitable for a wide range of development workflows.*

Additional resources:
* [Visual Studio Code Installation](https://code.visualstudio.com/download)
* [Git and VSCode](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git)
* [VSCode Linter](https://code.visualstudio.com/docs/python/linting)
* [VSCode Python Environment](https://code.visualstudio.com/docs/python/environments)


### Test Driven Development via pytest <a name="tdd"></a>

```
what is test driven development?
```

ChatGPT:

*Test-Driven Development (TDD) is a software development approach where tests are written before the actual code. The process emphasizes writing test cases for each small functionality and then developing the code to make those tests pass. Key features and steps of TDD include:*

1. *Write a Test: First, you write a unit test for a specific function or feature that will fail because the code doesn’t exist yet.*
2. *Run the Test: Run the test to confirm it fails, ensuring the test is valid and that the functionality is not yet implemented.*
3. *Write the Code: Develop the minimum amount of code required to make the test pass.*
4. *Run the Test Again: Run the test suite to check if the new code passes the test.*
5. *Refactor the Code: Clean up the code, optimizing it without changing its behavior, ensuring the tests still pass.*
6. *Repeat the Cycle: This process is repeated for every new feature or functionality, ensuring that all code is thoroughly tested.*

*Benefits of TDD:*
1. *Improves Code Quality: Since tests are written first, the code is generally more reliable, with fewer bugs.*
2. *Encourages Simplicity: Developers focus on writing just enough code to pass the tests, avoiding unnecessary complexity.*
3. *Facilitates Refactoring: Tests ensure that refactoring the code doesn’t introduce new bugs.*
4. *Promotes Better Design: Writing tests forces developers to think about the design and functionality of the code upfront.*

*In TDD, the code evolves in small, testable increments, ensuring that every piece of code is thoroughly tested and that the software remains functional as new features are added.*

```
what is pytest (concise)?
```

ChatGPT:

*Pytest is a popular Python testing framework that simplifies writing, organizing, and running tests. Key features include:*
1. *Simple syntax for writing tests as functions.*
2. *Auto-discovery of tests based on naming conventions.*
3. *Fixture support for setup and teardown of test environments.*
4. *Parameterization to run tests with multiple inputs.*
5. *Detailed error messages for failed assertions.*
6. *Extensible with a wide range of plugins.*

*It is widely used for unit, integration, and functional testing in Python projects.*

Additional resources:
* [Pytest pip](https://pypi.org/project/pytest/)
* [Pytest Docs](https://docs.pytest.org/en/stable/)
* [VSCode Pytest](https://code.visualstudio.com/docs/python/testing)


### Code Coverage via codecov and GitHub Actions <a name="codecov"></a>

```
what is code coverage?
```

ChatGPT:

*Code coverage is a software testing metric that measures the percentage of source code executed during testing. It helps assess how thoroughly a test suite exercises a program’s codebase, identifying untested parts of the code.*

*Code coverage can be measured in several ways, including:*

1. *Line Coverage: Measures how many lines of code are executed.*
2. *Branch Coverage: Evaluates whether all branches (e.g., if-else conditions) are tested.*
3. *Function/Method Coverage: Checks if all functions or methods have been called.*
4. *Statement Coverage: Assesses if every individual statement has been executed.*

*Higher code coverage suggests better testing but doesn't guarantee the absence of bugs or the quality of tests. It’s used to guide testing efforts and improve overall software reliability.*

Additonal resources:
* [Codecov](https://app.codecov.io/)
* [GitHub Actions](https://docs.github.com/en/actions)

### Markdown <a name="markdown"></a>

```
What is markdown (concise)?
```

ChatGPT:

*Markdown is a lightweight markup language that uses plain text formatting syntax to create formatted text. It is often used for writing documentation, README files, and content for the web, allowing for easy conversion to HTML.*

Additional resources:
* [Markdown VSCode](https://code.visualstudio.com/docs/languages/markdown)
* [Markdown Guide](https://www.markdownguide.org/getting-started/)

### Code Review <a name="review"></a>

```
What is code review?
```

ChatGPT:

*Code review is a systematic process in software development where one or more developers examine and evaluate another developer's code changes before merging them into the main codebase. The primary goals of code review are to ensure code quality, improve software design, identify bugs or security vulnerabilities, and share knowledge among team members.*

*Key aspects of code review include:*

1. *Feedback: Providing constructive criticism and suggestions for improvement.*
2. *Best Practices: Ensuring adherence to coding standards and conventions.*
3. *Collaboration: Facilitating communication and teamwork among developers.*
4. *Learning: Enhancing understanding of the codebase and different coding techniques.*

*Code reviews can be conducted through various methods, including pull requests, formal meetings, or using specialized tools.*

### Generative AI Policy <a name="genAI"></a>

The purpose of this course is to learn new skills. In my personal opinion, the biggest risk of using generative AI tools in this class is that you will deprive yourself of the opportunity to learn new skills in an environment with many resources to support you. That being said, it is completely normal to use any resources that you have access to to figure out how to solve problems while you are coding (e.g., [stackoverflow](https://stackoverflow.com/)). To this end, the core idealogical tenant of the course generative AI policy is that ultimately **you** are responsible for the accuracy and validity of the final products that you create, and **you** are responsible for what you get out of this course.

For english language text generated by AI, please indicate when you have used an AI tool to write any portion of the text (e.g., what I have done on this page). If you are unsure about what "counts" in this context, please err on the side of over-reporting generative AI use (e.g., "ChatGPT was used to write a first draft, available *here*, the final version reported on this page is the result of extensive edits to the generated text").

For every course assignment, please include in the relevant GitHub repository a text file titled "assignment_#_genAIuse.txt". In the text file, please state what tools were used and how. If you did not use any of these tools, please simply state "no AI tools were used to complete this assignment." We are collecting this data for information purposes only, as long as you take full responsibility for the functionality of the code you are allowed (though not necessarily encouraged) to use generative AI tools as a part of your workflow.

### Instructions for This Repository <a name="instructions"></a>

#### Get a copy of the repository on your local machine

The best way to do this is to create a GitHub account and ``clone`` the repository.

#### Create and activate a conda virtual environment

1. Install [Anaconda](https://docs.anaconda.com/anaconda/install/) on your local machine.
2. Open a ``Terminal`` session.
3. Type in the terminal to create a virtual environment with conda:
```bash
conda create --name setup-examples-env python=3.9.13
```
4. Type in the terminal to activate your virtual environment:
```bash
conda activate setup-examples-env
```
5. Check to make sure that the correct version of python is running (should be ``3.9.13``)
```bash
python --version
```
6. Update some base modules (just in case)
```bash
pip install --upgrade pip setuptools wheel
```

Note that once you have created this virtual environment you can ``activate`` and ``deactivate`` it in the future -- it is not necessary to create a new virtual environment each time you want to run this code, you can simply type ``conda activate setup-examples-env`` and then pick up where you left off.

#### Install setup-example

1. Use a ``Terminal`` session to navigate to the ``setup-example-main`` folder. The command ``cd`` will allow you to do this (see: )
2. Type the command ``ls`` and make sure that the file ``pyproject.toml`` is in the current directory.
3. Now, create an editable install of wound compute:
```bash
pip install -e .
```
4. If you would like to see what packages this has installed, you can type ``pip list``
5. You can test that the code is working with pytest (all tests should pass):
```bash
pytest -v --cov=setupexample  --cov-report term-missing
```
6. To run the code from the terminal, simply start python (type ``python``) and then type ``from setupexample import example_functions as ef``. For example:
```bash
(setup-examples-env) eml-macbook-pro:setup-example-main emma$ python
Python 3.9.13 | packaged by conda-forge | (main, May 27 2022, 17:01:00) 
[Clang 13.0.1 ] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> from setupexample import example_functions as ef
>>> ef.hello_world()
>>> "hello world!
```

#### Run the Tutorial

This GitHub repository contains a folder called ``tutorials`` that has a trivial example of a tutorial. The code can be run by navigating to the ``tutorials`` folder and running ``tutorials.py``.
