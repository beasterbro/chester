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
	This final chapter is about compiling the Kaleidoscope language into object
	files. 

8.2. Choosing a target
	Uses a target Triple to target the current machine. 

8.3. Target Machine
	Uses llc to get information about the current target machine.

8.4. Configuring the Module
	Configuring the module to specify the target and the specific data layouts.

8.5. Emit Object Code
	Defining where the compiler will write its file to.

8.6. Putting It All Together
	This section is just putting all the pieces of this chapter together in the
	compiler to generate output.o files. 

Their Tests

	Our Tests
	def average(x y z) (x + y + z) * 0.3333;

8.7. Full Code Listing
	This has the full final code for this tutorial since we are ending on this
	chapter of the tutorial. 