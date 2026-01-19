
# WLP4 Compiler

# About WLP4
WLP4 (Waterloo Language Plus Pointers Plus Procedures) is a subset of the programming language C with added constraints. 


A complete documentation of the language including specification of semantics and syntax can be found here: https://student.cs.uwaterloo.ca/~cs241/wlp4/WLP4.html. 

# Description
This project is a compiler that translates code in WLP4 into MIPS assembly. It includes three main stage: scanning, parsing, context-sensitive analysis and code generation. 

Scanning: 
- Implemented in wlp4scan.cc and dfa.cpp
- Converts the raw source code into a sequence of tokens, such as identifiers, keywords, operators, and literals.
- Uses a deterministic finite automaton (DFA) to recognize valid tokens efficiently.

Parsing: 
- Implemented in wlp4parse.cc, slr.cc, and wlp4parse.h
- Built a parse tree from the token stream using Syntactic Analysis (SLR(1) parsing).
- Verifies that the program structure conforms to the WLP4 grammar.
- Errors in syntax are reported appropriately. 

Semantic Analysis: 
- Implemented in wlp4type.cc
- Checks for semantic correctness that cannot be captured by syntax alone, including:
    - Type checking of expressions
    - Variable declaration and usage
    - Function argument verification

Code Generation: 
- Implemented in wlp4gen.cc and asm.cpp
- Translates the validated parse tree into MIPS assembly code. 
- Produces an output that can be executed using a MIPS simulator.

The source code of this project is not publicly released in accordance with the University of Waterloo's policies. If you would like to see the source code, please reach me at j92deng@uwaterloo.ca. 
