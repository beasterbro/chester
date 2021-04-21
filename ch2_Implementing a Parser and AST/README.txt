Name:		Emily Howell	Adam Stewart 	Ally Dinhofer 
Case ID: 	eth35 		axs1477		abd54

____________________________________________________________________________________

https://llvm.org/docs/tutorial/MyFirstLanguageFrontend/LangImpl02.html#full-code-listing
____________________________________________________________________________________


Compilation:
clang++ -g -O3 toy.cpp `llvm-config --cxxflags` -o toy

Running it:
./toy

____________________________________________________________________________________
____________________________________________________________________________________


2.1. Chapter 2 Introduction
	Just explaining the next steps. We have the lexer and now we need to make 
	the parser. Once the parser is completed we will make an AST. 

2.2. The Abstract Syntax Tree (AST)
	Creating objects for each construct in the Kaleidoscope language. The three 
	constructs covered here are expressions, prototypes, and functions. It starts 
	by creating a base expression class, ExprAST, and then creating NumberExprAST,
	VariableExprAST, BinaryExprAST, CallExprAST that all inherit the base class. 
	In this subchapter we also define PrototypeAST and FunctionAST for the last 
	two constructs in the Kaleidoscope language.

2.3. Parser Basics
	Creates the basic structures of the parser that will be expanded upon in 
	further subsections. Creates CurrTok, a token buffer around the lexer that 
	holds the current token. Also implements basic structures for error handling.

2.4. Basic Expression Parsing
	Covers the variety of different types of expression handling. 

2.5. Binary Expression Parsing
	Covers the complications of ambiguous parsing when it comes to binary 
	expressions. This parser will be using Operator-Precedence Parsing to handle
	any ambiguity. 

2.6. Parsing the Rest
	Covers how to parse prototypes, definitions, externs, and top-level-expressions.

2.7. The Driver
	The driver connects all of the parts together by iterating through the tokens
	and directing them to the appropriate section of the parser. 

2.8. Conclusions
	This section covers the compilation and testing of the parser, lever, and AST.
	
	Tests used in the tutorial:
		def foo(x y) x+foo(y, 4.0);	<-- recursive function definition
		def foo(x y) x+y y; 		<-- normal function definition
		def foo(x y) x+y ); 		<-- function definition with error
		extern sin(a); 			<-- extern definition

	Our tests:
		def cat(x y z) x+foo(y, z, 3.0); 	<-- recursive function definition
		def cat(x y z) x+y y;		<-- normal function definition
		def cat(x y z) x+y &;		<-- function definition with error
		extern cos(a); 			<-- extern definition

	The output of our tests can be found in ch2_test.png.

2.9. Full Code Listing
	The complete code developed in this chapter of the tutorial. This was 
	compiled into toy.cpp. 
____________________________________________________________________________________

Notes:

(1)	For this chapter I added an empty main function to the end of it to verify that it 
	would compile. I also had to add '#include <string>' to the top so that it would
	compile properly. The instructions in the tutorial didn't have any explained 
	method for testing this code out in this chapter so I am going to move onto the
    	next chapter without doing so.