
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#features">Features</a></li>
         <li><a href="#parsing">Parsing</a></li>
        <li><a href="#execution">Execution</a></li>
        <li><a href="#examples" >Examples</a></li>
      </ul>
    </li>
    <li><a href="#upcoming-features">Upcoming Features</a></li>
    <li><a href="#how-well-python-was-used?">How Well Python was Used?</a></li>
    <li><a href="#limitations">Limitations</a></li>
    <li><a href="#References">References</a></li>
  </ol>
</details>



>If you don't know how compilers work, then you don't know how computers work.     --Steve Yegge

<!-- ABOUT THE PROJECT -->
## About The Project


Lisp is the second-oldest high-level programming language and first functional language.It is the backbone for many dialectsl like Common Lisp, Scheme, Racket and Clojure.Lisp was used for Artificial Intelligence. This repo implements Lisp Interpreter in Python 3. 



### Built With


* [Python](https://docs.python.org/3/)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started



### Installation


1. Clone the repo
   ```sh
   https://github.com/tsk1729/Lisp-Interpreter.git
   ```
2. Type the command 
  ```Python3 lisp.py```
3. Lisp Interpreter is ready with Prompt.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->

### Features

- Core lisp language `if`, `let`, `car`, `lambda`, `cons`, `cdr`,`?eq`,`lenght` etc.
- Subset of scheme : lists, real numbers, characters, strings.
- Easy to integrate Python functions.
- REPL for interactive command line tool.
- Supported in Python2 and Python3.
- Efficient parsing.
- Local and Globe Scope Separation
- Small(117 lines) DecentFast(0.03 s for Factorial(100) Program)

<p align="right">(<a href="#top">back to top</a>)</p>





The language interpreter has two parts:
### Parsing: 
The parsing component takes an input program in the form of a sequence of characters, verifies it according to the syntactic rules of the language, and translates the program into an internal representation. In a simple interpreter the internal representation is a tree structure (often called an abstract syntax tree) that closely mirrors the nested structure of statements or expressions in the program. In a language translator called a compiler there is often a series of internal representations, starting with an abstract syntax tree, and progressing to a sequence of instructions that can be directly executed by the computer. Above program has  a parser is implemented with the function parse.

### Execution:
The internal representation is then processed according to the semantic rules of the language, thereby carrying out the computation. Lispy's execution.

            program ➡ parse ➡ abstract-syntax-tree ➡ eval ➡ result 

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- Limitations -->
### Examples:
```
>>> repl()
lis.py> (define circle-area (lambda (r) (* pi (* r r))))
lis.py> (circle-area 3)
28.274333877
lis.py> (define fact (lambda (n) (if (<= n 1) 1 (* n (fact (- n 1))))))
lis.py> (fact 10)
3628800

```

## Upcoming Features

- Running Lisp program files along with interactive shell.


## How well  Python was used
- Easy environment scope using dictionaries.
- Creation Of Abstract Syntax Tree using Lists
- Class instaces behaving like fuctions using [__call__](https://www.geeksforgeeks.org/__call__-in-python/)
- Operator module short notations for most of math functions.
- Object orientated feaures of Python for local and global scopes. 

### Limitations

- Error recovery: Above interpreter does not attempt to detect, reasonably report, or recover from errors. Lispy expects the programmer to be perfect. 
- Missing Datatypes like integers etc.
- Missing call/cc and tail recursion. 

<!--References -->
### References


* [Jscheme Java Lisp Interpreter](http://norvig.com/jscheme.html)
