Name:		Emily Howell	Adam Stewart 	Ally Dinhofer 
Case ID: 	eth35 		axs1477		abd54

____________________________________________________________________________________

https://llvm.org/docs/tutorial/MyFirstLanguageFrontend/LangImpl03.html
____________________________________________________________________________________


Compilation:
clang++ -g -O3 toy.cpp `llvm-config --cxxflags --ldflags --system-libs --libs core` -o toy

Running it:
./toy

____________________________________________________________________________________
____________________________________________________________________________________


3.1. Chapter 3 Introduction
	This chapter of the tutorial covers how to turn the AST from the previous
	chapter into LLVM IR.

3.2. Code Generation Setup
	Define codegen() methods in each class. This simply instructs the AST to
	generate IR for for that AST node and then return an LLVM Value object.
	This section also covers creating a virtual method to implement a visitors
	pattern as well as an error logging functionality. 

3.3. Expression Code Generation

3.4. Function Code Generation

3.5. Driver Changes and Closing Thoughts
	
	Tests used in the tutorial:
		4+5;	<-- recursive function definition
		def foo(a b) a*a + 2*a*b + b*b; 		<-- normal function definition
		def bar(a) foo(a, 4.0) + bar(31337);		<-- function definition with error
		extern cos(x); 			<-- extern definition
		^D

	Our tests:
		3+4;	<-- recursive function definition
		def got(a b) a+a * 2+a+b * b+b; 		<-- normal function definition
		def cat(a) got(a, 3.0) + cat(1337);		<-- function definition with error
		extern sin(x); 			<-- extern definition
		sin(1.234);
		^D

3.6. Full Code Listing