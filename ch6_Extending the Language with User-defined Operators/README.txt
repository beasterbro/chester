Name:		Emily Howell	Adam Stewart 	Ally Dinhofer 
Case ID: 	eth35 		axs1477		abd54

____________________________________________________________________________________

https://llvm.org/docs/tutorial/MyFirstLanguageFrontend/LangImpl06.html
____________________________________________________________________________________


Compilation:
clang++ -Xlinker --export-dynamic -g toy.cpp `llvm-config-12 --cxxflags --ldflags --system-libs --libs core orcjit native` -O3 -o toy

Running it:
./toy

____________________________________________________________________________________
____________________________________________________________________________________


6.1. Chapter 6 Introduction
	This section focuses on adding user defined operators to the language.

6.2. User-defined Operators: the Idea
	

6.3. User-defined Binary Operators

6.4. User-defined Unary Operators

6.5. Kicking the Tires

	Tests used in the tutorial:
	extern putchard(char);
	def foo(d) d < 8;
	def printdensity(d) if foo(d) then putchard(42) else 0;
	printdensity(1);
	printdensity(9);

We had to nest our if statements so that the functions successfully compile
	Our tests:
	extern putchard(char);
	def foo(d) d < 8;
	def printdensity(d) if foo(d) then putchard(42) else 0;
	printdensity(1);
	printdensity(9);

6.6. Full Code Listing