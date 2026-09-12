# Compiler Architecture

This project implements a compiler for the Tiger programming language. Its design follows a traditional multi-stage compiler pipeline:

```text
Tiger source code
        ↓
Lexical analysis
        ↓
Parsing
        ↓
Abstract syntax tree
        ↓
Semantic analysis
        ↓
HERA code generation
```

Lexical analysis is implemented with Flex, using `tiger-lex.ll`. The lexer identifies tokens such as keywords, identifiers, literals, operators, and punctuation.

The grammar in `tiger-grammar.yy` is processed by Bison. It validates the structure of a Tiger program and constructs the abstract syntax tree.

The AST is implemented across files such as `AST.cpp`, `AST.h`, and `AST_appel.h`. Additional files provide tree traversal and analysis functionality.

Semantic analysis is handled by the type-checking and symbol-table components. These stages verify that identifiers are declared, expressions use compatible types, and functions and variables are used correctly.

Finally, the compiler generates HERA code and data using `HERA_code.cpp` and `HERA_data.cpp`. CMake is used to build the compiler and organize the generated parser and lexer files.
