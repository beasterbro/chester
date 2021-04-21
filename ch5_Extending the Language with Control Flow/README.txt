Name:		Emily Howell	Adam Stewart 	Ally Dinhofer 
Case ID: 	eth35 		axs1477		abd54

____________________________________________________________________________________

https://llvm.org/docs/tutorial/MyFirstLanguageFrontend/LangImpl05.html
____________________________________________________________________________________


Compilation:
clang++ -g toy.cpp `llvm-config --cxxflags --ldflags --system-libs --libs core orcjit native` -O3 -o toy

Running it:
./toy

____________________________________________________________________________________
____________________________________________________________________________________


5.1. Chapter 5 Introduction
	This chapter of the tutorial adds in the functionality to handle conditional
	branches. 

5.2. If/Then/Else
	In order to add conditional support to the compiler you just need to add
	support to the lever, AST, parser, and LLVM code emitter. 

5.3. ‘for’ Loop Expression
	Similarly to the conditional support in 5.2, in order to add support for 
	looping we have to simply add the concept to the lever, AST, parser, and 
	LLVM code emitter. 

Since there were no tests for this chapter we elected to use our previous tests to ensure we did not lose any functionality 	

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

5.4. Full Code Listing
	This section has all the code used for this chapter of the tutorial.
