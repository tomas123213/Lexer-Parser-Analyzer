# Lexer-Parser-Analyzer
## About the Project
Lexer and Parser program was a 2 part program that was assigned as a project during my Programming Languages class.
CLite is our simplified programming language that looks a little like C and Java. In this assignment we completed the lexical analyzer (lexer) for CLite.

These programs were written using PyCharm. I have uploaded what I completed during the school year but since we did not use GitHub for the class there is no step by step commit available. 
The Lexer was Part 1 of the assignment. In order to test the lexer I used the lexertest.c file that is available in the repository.
The Parser was Part 2 of the assignment which builds upon Part 1. In order to test the Parser, I ran it using the test.c file that is also available within the repository. 

## Language Rules Given by Professor
The Language that we had to follow for Part 2 is below.
  Program         ⇒  int  main ( ) { Declarations Statements } <br />
  Declarations    ⇒  { Declaration } <br />
  Declaration     ⇒  Type  Identifier  ; <br />
  Type            ⇒  int | bool | float <br />
  Statements      ⇒  { Statement } <br />
  Statement       ⇒  ; | Block | Assignment | IfStatement  <br />
                       | WhileStatement | PrintStatement
  Block           ⇒  { Statements }
  Assignment      ⇒  Identifier = Expression ;
  IfStatement     ⇒  if ( Expression ) Statement [ else Statement ]
  WhileStatement  ⇒  while ( Expression ) Statement 
  PrintStatement  ⇒  print( Expression ) ;  
  Expression      ⇒  Conjunction { || Conjunction }
  Conjunction     ⇒  Equality { && Equality }
  Equality        ⇒  Relation [ EquOp Relation ]
  EquOp           ⇒  == | != 
  Relation        ⇒  Addition [ RelOp Addition ]
  RelOp           ⇒  < | <= | > | >= 
  Addition        ⇒  Term { AddOp Term }
  AddOp           ⇒  + | -
  Term            ⇒  Factor { MulOp Factor }
  MulOp           ⇒  * | / | %
  Factor          ⇒  [ UnaryOp ] Primary
  UnaryOp         ⇒  - | !
  Primary         ⇒  Identifier | IntLit | FloatLit | ( Expression ) | true | false

## Part 1: Running just the lexer on lexertest.c file. Should return all the tokens, legal and illegal, and their line number.
![image](https://user-images.githubusercontent.com/35609863/47688890-ba8e7400-dbbd-11e8-99ad-a27a9d45898a.png)

![image](https://user-images.githubusercontent.com/35609863/47688900-c8dc9000-dbbd-11e8-9f0e-b0a8915c9127.png)

![image](https://user-images.githubusercontent.com/35609863/47688903-ced27100-dbbd-11e8-81ef-8f7c0840f73d.png)

## Part 2: Running the parser, which uses the lexer, on test.c file. Should return the same format as before and follow the rules of the language provided.

![image](https://user-images.githubusercontent.com/35609863/47688984-37215280-dbbe-11e8-99ed-e98ac2963bbb.png)
