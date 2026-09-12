# Error Reporting

Compiler diagnostics are implemented through `errormsg.cpp` and `errormsg.h`.

The error-reporting system is used to identify invalid source programs and provide feedback during compilation. Errors may originate from lexical analysis, parsing, or semantic analysis.

Typical diagnostic categories include:

- Invalid or unexpected characters
- Syntax errors
- Undeclared identifiers
- Invalid type usage
- Incorrect function arguments
- Invalid assignments
- Improper loop or control-flow usage

The parser and compiler stages pass source-location information to the diagnostic system so that errors can be associated with the relevant part of the input.

Centralizing diagnostics avoids duplicating error-handling logic throughout the compiler and provides a consistent interface for reporting problems.
