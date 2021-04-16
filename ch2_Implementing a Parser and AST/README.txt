Name:		Emily Howell	Adam Stewart 	Ally Dinhofer 
Case ID: 	eth35 		axs1477		abd54

____________________________________________________________________________________

https://llvm.org/docs/tutorial/MyFirstLanguageFrontend/LangImpl02.html#full-code-listing
____________________________________________________________________________________

2.1. Chapter 2 Introduction
    Just explaining the next steps. We have the lexer and now we need to make the 
        parser.  

2.2. The Abstract Syntax Tree (AST)
    Creating objects for each construct in the Kaleidoscope language. The three 
        constructs covered here are expressions, prototypes, and functions. 
	The Lexer breaks the input into Tokens. First it removed the whitespace, then 
		identifies keywords, then handles comments, and lastly identifies operator 
		characters. I compiled all of the code for this subsection into the file 
		lexer.cpp.

2.3. Parser Basics

2.4. Basic Expression Parsing

2.5. Binary Expression Parsing

2.6. Parsing the Rest

2.7. The Driver

2.8. Conclusions

2.9. Full Code Listing

For this chapter I added an empty main function to the end of it to verify that it 
	would compile. I also had to add '#include <string>' to the top so that it would
	compile properly. The instructions in the tutorial didn't have any explained 
	method for testing this code out in this chapter so I am going to move onto the
    next chapter without doing so.