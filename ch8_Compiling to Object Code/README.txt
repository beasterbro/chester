Name:		Emily Howell	Adam Stewart 	Ally Dinhofer 
Case ID: 	eth35 		axs1477		abd54

____________________________________________________________________________________

https://llvm.org/docs/tutorial/MyFirstLanguageFrontend/LangImpl08.html
____________________________________________________________________________________


Compilation:
clang++ -g -O3 toy.cpp `llvm-config --cxxflags --ldflags --system-libs --libs all` -o toy

Running it:
./toy

____________________________________________________________________________________
____________________________________________________________________________________


8.1. Chapter 8 Introduction

8.2. Choosing a target

8.3. Target Machine

8.4. Configuring the Module

8.5. Emit Object Code

8.6. Putting It All Together

8.7. Full Code Listing