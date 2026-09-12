# Symbol Tables and Scope Handling

The compiler uses symbol-table structures to associate identifiers with the information required during compilation. This includes variables, functions, and type-related information.

Symbol and table definitions are provided by files such as `symbol.h`, `ST.h`, and `ST.cpp`.

Scope handling is important because Tiger programs may contain nested blocks, local declarations, and functions. When a new scope is entered, declarations introduced in that scope must be available to the code inside it. When the scope ends, those declarations must no longer be visible.

The symbol-table implementation supports operations such as:

- Adding declarations
- Looking up identifiers
- Handling nested scopes
- Distinguishing identifiers with the same name in different scopes
- Associating identifiers with types or other compiler metadata

The project also includes traversal utilities such as `parent.cpp`, `loop_parent.cpp`, and `depth.cpp`, which support analysis of AST relationships and nesting.
