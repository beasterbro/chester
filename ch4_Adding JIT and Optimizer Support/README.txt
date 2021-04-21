Name:		Emily Howell	Adam Stewart 	Ally Dinhofer 
Case ID: 	eth35 		axs1477		abd54

____________________________________________________________________________________

https://llvm.org/docs/tutorial/MyFirstLanguageFrontend/LangImpl04.html
____________________________________________________________________________________


Compilation:
clang++ -g toy.cpp `llvm-config-12 --cxxflags --ldflags --system-libs --libs core orcjit native` -O3 -o toy

Running it:
./toy

____________________________________________________________________________________
____________________________________________________________________________________


4.1. Chapter 4 Introduction
	In this chapter of the tutorial we add JIT compiler support and optimizer
	support. 

4.2. Trivial Constant Folding
	Constant folding is explained to be important for optimization but apparently
	is not useful in the case of the AST. 

4.3. LLVM Optimization Passes
	This section covers the optimization passes built into LLVM. LLVM supports
	whole module passes as well as per function passes. This means there is 
	support for passes over large bodies of code as well as single functions.

4.4. Adding a JIT Compiler
	
	Tests used in the tutorial:
		def foo(x) x + 1;
		foo(2);
		def foo(x) x + 2;
		foo(2);
		extern sin(x);
		extern cos(x);
		sin(1.0);
		def foo(x) sin(x)*sin(x) + cos(x)*cos(x);
		foo(4.0);

	Our tests:
		def cat(x) x + 4;
		cat(2);
		def cat(x) x + 5;
		cat(2);
		extern sin(x);
		extern cos(x);
		sin(1.0);
		def cat(x) sin(x)*sin(x) + cos(x)*cos(x);
		cat(4.0);

4.5. Full Code Listing
	This section has all of the code used for this chapter.