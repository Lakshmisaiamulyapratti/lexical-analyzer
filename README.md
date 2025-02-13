# Lexical Analyzer 
The OCaml program that is implemented here is a common or basic tokenizer that is used in classifying an input string into tokens and these tokens are further categorized into Keywords, Operators, Punctuation, Integer Literals, Identifiers or also as Unknown on the basis of predefined sets & patterns that are given in the code.

## Features:-
- Here, it identifies and also classifies some common programming constructs like "Keywords" such as if, else, while, etc., "Operators" such as +, -, *, etc.,  "Punctuation" such as {, }, ;, etc.,

- Also, identifies some integer literals and identifiers that are valid on the basis of a given set of rules.

- This mainly supports basic method of classification of input string that is given into tokens there by allowing it to parse some expressions that are simple too.

## Structure:-
### Types:-
- Here, the program defines 6 types of tokens;
```ocaml
type token =
  | Keyword of string
  | Operator of string
  | Punctuation of string
  | IntLiteral of int
  | Identifier of string
  | Unknown of string
```
### Functions:-
#### Keywords, Operators, Punctuation:- 
- Gives a list that consists of some predefined sets of keywords, operators and punctuation.

#### is_identifier:-
- It verifies whether a given input string is valid identifier or not on the basis of a set of rules like it starts with a letter or underscore, whether it is followed by alphanumeric characters / underscores.

#### classify_token:-
##### After taking an input string as input, it classifies that input string into one of the token categories that are given below:-
- Keyword:- If the given input string matches to any one of the keywords that are predefined.

- Operator:- If the given input string matches to any one of the operators that are predefined.

- Punctuation:- If the given input string is having any punctuation symbol.

- IntLiteral:- If the given input string is an integer that is valid.

- Identifier:- If the given input string strictly follows some rules of an identifier.

- Unknown:- If the given input string does not match with any one of the above categories given. 

#### tokenize:-
- Here, it tokenizes a given input string by first splitting it into sub strings on the basis of delimiters present in the input string and next it classifies each sub string into the token type that it belongs to and in this process it utilizes a function called 'split_aux' to split the input string into a list of tokens.

#### main function:-
- Here, the program is compiled and run in the Ubuntu command prompt by taking an input string from the user and then classifying that string and printing the list of tokens that are generated.

### Sample Test Case:-
Enter input string: let y = 2 + 7;
Generated tokens from the given input string:
Keyword: let
Identifier: y
Operator: =
IntLiteral: 2
Operator: +
IntLiteral: 7
Punctuation: ;

## How to compile & run in the Ubuntu command prompt:-
- First, we open the Ubuntu command prompt and redirect into the directory where our code has been saved.

- Next, we compile the code by using below command:-

``` ocamlc -o tokenizer tokenizer.ml ```

- After, we run the code by using the below command:-

``` ./tokenizer ```

