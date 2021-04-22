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
	This section just covers the concept of user defined operators and how this
	concept appears, or rather doesn't, in C++.

6.3. User-defined Binary Operators
	Extend the PrototypeAST function to support user defined binary operators.
	After this we also need to be able to determine whether it was an operator, 
	and if it was, what precedence level the given operator has which can be done
	through parsing the prototype. Lastly, we added support for binary operators
	in codegen. 

6.4. User-defined Unary Operators
	Unary operators aren't supported at all in the kaleidoscope language so the
	support for them and any user defined versions of them have to be added to
	the compiler code. 

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
	This section has the fully updated code for this section.