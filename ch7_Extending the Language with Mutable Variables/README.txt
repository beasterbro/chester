Name:		Emily Howell	Adam Stewart 	Ally Dinhofer 
Case ID: 	eth35 		axs1477		abd54

____________________________________________________________________________________

https://llvm.org/docs/tutorial/MyFirstLanguageFrontend/LangImpl07.html
____________________________________________________________________________________


Compilation:
clang++ -Xlinker --export-dynamic -g toy_udf.cpp `llvm-config-12 --cxxflags --ldflags --system-libs --libs core orcjit native` -O3 -o toy

Running it:
./toy

____________________________________________________________________________________
____________________________________________________________________________________


7.1. Chapter 7 Introduction
	This chapter is about implementing mutable variables. 

7.2. Why is this a hard problem?
	SSA form requires nontrivial algorithms and data structures and mutable 
	variables can't be in SSA form.

7.3. Memory in LLVM
	Register values have to be in SSA form but memory objects don't have to be.
	Therefore, we can make a stack variable for each mutable object defined in a 
	function to get around this.

7.4. Mutable Variables in Kaleidoscope
	We are adding two abilities to the language: the ability to mutate variables
	with the '=' symbol and the ability to define new variables. 

7.5. Adjusting Existing Variables for Mutation
	Some refactoring has to be done because NamedValues needs to be able to map
	to the memory location of the variable. 

7.6. New Assignment Operator

Our Tests

extern printd(x);
def binary : 1 (x y) y;
def rest(y)  printd(y) :  y = 3 :  printd(y);
rest(333);

7.7. User-defined Local Variables
	Alters a slew of different methods including ParsePrimary() and ParseVarExpr()
	in order to allow for some trivial implementation of mutable local vars. 

7.8. Full Code Listing
	This section has the fully updated compiler code for this chapter. 
