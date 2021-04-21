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

7.2. Why is this a hard problem?

7.3. Memory in LLVM

7.4. Mutable Variables in Kaleidoscope

7.5. Adjusting Existing Variables for Mutation

7.6. New Assignment Operator

Our Tests

extern printd(x);
def binary : 1 (x y) y;
def rest(y)  printd(y) :  y = 3 :  printd(y);
rest(333);

7.7. User-defined Local Variables

7.8. Full Code Listing
