# Code Generation

After parsing and semantic analysis, the compiler translates the validated AST into HERA assembly.

Code generation is implemented primarily in `HERA_code.cpp` and `HERA_data.cpp`.

The code-generation stage handles both executable instructions and data required by the program. It translates high-level constructs such as:

- Arithmetic expressions
- Variable access
- Assignments
- Conditional statements
- Loops
- Function calls
- Return expressions
- String or other static data

The compiler tracks intermediate results while traversing the AST. Supporting files such as `result_reg.cpp` and `result_reg_reset_kludge.h` help manage result registers during expression translation.

Separate handling for code and data allows generated instructions to be organized independently from static values. The resulting HERA output can then be inspected or executed using the project’s testing workflow.
