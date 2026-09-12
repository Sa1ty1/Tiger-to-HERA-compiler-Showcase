# AST Design

The compiler represents parsed Tiger programs with an abstract syntax tree rather than processing source text directly after parsing.

The AST removes unnecessary grammar details and represents the meaningful structure of a program, including:

- Expressions
- Variables
- Function calls
- Declarations
- Assignments
- Conditional expressions
- Loops
- Blocks
- Integer and string literals

The main AST implementation is contained in `AST.cpp` and `AST.h`. `AST_appel.h` provides additional AST-related definitions based on the Tiger language design.

Separate traversal programs, including `AST-print.cpp` and `AST-print-attributes.cpp`, demonstrate how the tree can be inspected and how node attributes can be displayed.

Using an AST makes later compiler stages independent from the original source formatting. Type checking, tree analysis, and code generation can operate on a structured representation of the program.
