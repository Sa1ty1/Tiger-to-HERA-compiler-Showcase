# Tiger-to-HERA-compiler-Showcase
A showcase of my Compiler Project, as the actual code must stay private for academic restrictions.

A compiler project for a Tiger-like programming language, translating source programs into HERA assembly. The project demonstrates the complete compiler pipeline, from lexical analysis and parsing through semantic validation, abstract syntax tree processing, and code generation.

### Key Features

- Lexical analysis using Flex
- Grammar parsing using Bison
- Abstract syntax tree construction and traversal
- Symbol-table management and scope handling
- Type checking and semantic analysis
- Variable, function, loop, and expression processing
- HERA code and data generation
- Compiler diagnostics and error reporting

### Technical Focus

This project provided practical experience with compiler architecture, recursive data structures, parsing theory, static analysis, memory representation, and assembly-level code generation. Supporting documentation covers the AST design, coding standards, source organization, and compiler usage.


### This repo outline

See /docs for explainations of how the Compiler was built and works.
See /examples for images and videos of the program compiling a Tiger program as input and producing HERA code that is then run and should output the result of the Tiger program.


## Example Compilations, including error handling

![Watch the first test example](https://youtu.be/1kJBgOJ5QZY)

![Watch the second test example](https://youtu.be/e2fqfMz2ZFE)

![Error handling demonstration](examples/test_7_33_error/error-handling.png)