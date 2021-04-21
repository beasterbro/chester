Name:		Emily Howell	Adam Stewart 	Ally Dinhofer 
Case ID: 	eth35 		axs1477		abd54

____________________________________________________________________________________

https://llvm.org/docs/tutorial/MyFirstLanguageFrontend/LangImpl06.html
____________________________________________________________________________________


Compilation:
clang++ -Xlinker --export-dynamic -g toy_udf.cpp `llvm-config-12 --cxxflags --ldflags --system-libs --libs core orcjit native` -O3 -o toy

Running it:
./toy

____________________________________________________________________________________
____________________________________________________________________________________


6.1. Chapter 6 Introduction

6.2. User-defined Operators: the Idea

6.3. User-defined Binary Operators

6.4. User-defined Unary Operators

6.5. Kicking the Tires


	Tests used in the tutorial:

		extern putchard(char);
		def printdensity(d):  if d > 8 then
    putchard(32)  # ' '
  else if d > 4 then
    putchard(46)  # '.'
  else if d > 2 then
    putchard(43)  # '+'
  else
    putchard(42); # '*'

printdensity(1): printdensity(2): printdensity(3):
       printdensity(4): printdensity(5): printdensity(9):
       putchard(10);
**++.
mandel(-2.3, -1.3, 0.05, 0.07);


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



6.6. Full Code Listing