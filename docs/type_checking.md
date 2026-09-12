# Type-Checking Strategy

Type checking is performed after parsing and AST construction. Its purpose is to detect semantic errors that cannot be identified by the lexer or parser alone.

The implementation is distributed across `type_checking.cpp`, `types.cpp`, and `types.h`.

The compiler verifies that:

- Variables are used with compatible values
- Operators receive valid operand types
- Conditions use appropriate expressions
- Assignments match the declared type
- Function arguments match parameter types
- Function results match declared return types
- Arrays and records are used consistently
- Referenced identifiers have been declared

Type information is propagated through AST expressions. Each expression can be analyzed to determine the type it produces, allowing enclosing expressions and statements to be checked.

This stage separates syntactic correctness from semantic correctness. A program may be grammatically valid while still being rejected because of an undeclared identifier or incompatible types.
