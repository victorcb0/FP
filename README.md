# FP (Functional Programming - CLISP - OCaml)
Functional Programming (FP), represented here by the CLISP and OCaml languages, is a programming paradigm that focuses on using pure functions to handle computation. By avoiding state change and data mutability, FP promotes mathematical functions without side effects. CLISP provides an interactive programming environment based on the Common Lisp standard, while OCaml is a functional and statically typed programming language. The following labs apply these concepts and work on various problems to strengthen your understanding of FP and familiarize you with CLISP and OCaml.

## Laboratory 1 - CLisp

3. Translate the following expressions into LISP and then evaluate them:
- (25 + 30) * 15/2
- 6 * 3.1416

4. Determine the integer quotient for the arithmetic mean of the numbers:
- 5, 6.7, -23.2, 75 și 100.3

5. Determine the remainder of the division of the numbers:
- 365 12, 13 şi 467

6. Write the solutions of the following quadratic equation as LISP expressions, then evaluate the expressions:
- 2x2 +7x +5 = 0

7. Determine the integer result by rounding down and up, respectively, and then incrementing and decrementing the result for the following expression:
- (5 * 2.25 – 7.13) / (45 – 25 / 5)

8. Rate the following shapes:
- (* (MAX 3 4 5) (MIN 3 4 5))
- (EXPT (MAX 3 1 4) (MAX 2 7 1))
- (REM (+ 5 7 13) (- 14 1))

9. Display the output from problem 3 as a message:
- Ex: the remainder of the division of the numbers ... and ... is: ...

10. Display a message before reading a variable, then read the variable.
- Ex: "a =" reading value

## Laboratory 2 - CLisp

1. Remove the symbol D from the following expressions used CAR and CDR.
- (A B C D)
- (A (B C) (D E))
- (A (B C (D E)))
- ((A) (B) (C) (D) (E))
- ( A (B) ((C)) (((D))) ((((E)))))
- ((((A) B) C) D)

2. Evaluate the following Lisp expression, then return the length of the resulting list:
- (subst ' azi ' maine (reverse ' (frumoasa zi o este maine)))

3. Evaluate the following expressions in order and justify the result:
- (setq lista ’(a b c (d e))
- (setq M ’max)
- (cons M lista)
- (cons lista M)
- (append (list M) (last (cdr lista)))
- (list ' M (cadr lista))
- (append ' lista (list M (last lista)))
- (list (car lista) (cadr lista) (caddr lista) M)

4. The list is considered:
- ((A) (B) (C) (D) (E))

Using all the list construction and list access functions, construct the following list:
- ((((A) (B) (C)) . B) (E D C) D)

The solution that includes all the presented predefined functions is evaluated with the highest grade.

5. The list is considered:
- l1: ((((A) (B)) C) (D) (EF G))

Correct the error that occurred after evaluating the expression:
- (append (cadr l1) (car (nth '1 l1)) (last l1))
Then argue the result of evaluating the expression:
- (cons (nth '3 l1) (nthcdr '2 l1))

6. Evaluating the following expressions yields the results:
- (setq E '(x y ((z) u)) F (last E) G (caar F)) - (Z)
- (setq X '12 Y '14 Z '22 E (- (+ x y) z)) - 4
- (setq M (MIN 1 -4 23 56 1) P (* M 10) X (EXPT P 2)) - 1600

Evaluate the symbols for each expression separately and argue the result.

7. The list is considered:
- (A B C D)

Using the SUBST function together with other functions, obtain from the initial list the list:
- (D B C A)

Using the REVERSE function together with other functions, obtain from the initial list, the list:
- (D A B C)

## Laboratory 3 - CLisp

1. Use if to express the modulus of a number and the not operator:
- (abs x) (not y)

2. Express with the help of cond : and, or between 3 arguments:
- (or x y z) (and u v w)

3. Determine with the help of cond the middle element among three numerical elements.

4. Define the functions my-third, my-last, which return the third element of a list, respectively the last element of a list.

5. Define a my-append function that takes two list arguments and returns a double-length list obtained by concatenating the two original lists. Then you define the palindrome predicate that determines whether the resulting list is palindrome or not.

6. Define a function that receives as parameters the coefficients of a degree 2 equation and that if delta is positive returns a list of the solutions of the equation, if delta is equal to 0, returns the unique solution of the equation of degree 2, and if delta is negative, returns the message "complex solutions".

7. Define a function that takes a single argument x and returns the value of a function defined like this:

![picture alt](https://github.com/victorcb0/FP/blob/main/Laborator%203/Ex%207%20-%20Functie.png)

8. Define a function that receives as arguments an atom and a list, and returns a list in which the atom is added to the tail of the initial list, only if the atom is not found in the list. Otherwise, the list fragment starting with the found element is returned.

9. Define a function that displays an interactive menu, reads one character at a time and performs an operation according to the character read, and if the character is not one of the characters read, returns an error message.
- 1 – Addition
- 2 – Substraction
- 3 – Multiplication
- 4 – The remainder of the division

Consider three initialized variables with values read from the keyboard, the first two represent two integers, and the last one, the number corresponding to the operation to be executed. In the body of LET, the operation corresponding to the read character is executed for the third variable.

10. Recursively implement a COUNTATOMS function that receives as an argument a list that also contains nested lists and returns the total number of elements of the list.

11. Implement the Rot-left and Rot-right recursive functions that rotate left and right n elements of a list. Left rotation means moving the first element of the list to the end of the list. Right rotation means moving the last element of the list to the front of the list.

12. Write a function no_duplicates ( list ) that returns the list without duplicates. The elements should be in the same order in the returned list as in the initial list, keeping the last appearance of the duplicate elements.
- Example: > ( f a r a _d u b l u r i ‟ ( 1 2 2 3 4 5 6 4 4 ) )  ( 1 2 3 5 6 4 )

13. Recursively implement the presentp predicate that determines whether an atom appears anywhere within a list, even a list that contains nested lists.

14. Recursively implement a function that takes an integer as an argument and returns the list of the number's digits.

15. Iteratively implement the pozpar function, which takes a list as an argument and returns a list with the elements in the odd positions of the original list.

16. Iteratively implement a function that determines the greatest common divisor of two integers. Highlight the current parameters and the resulting value of the called function, in the order of the calls, respectively the terminations of the function for a concrete example.

## Laboratory 4 - CLisp

1. Implement a function that adds all the elements of a list, located in even positions. Positions are considered starting from 0.

2. Recursively implement the union, intersection, and difference of 2 sets using remove-if-not.

3. Define a function that counts the occurrences of a given number in a generalized list, using mapcar and lambda.

4. Define a function that displays a generalized list in the form specified for the following example:
- (a b (c d) (e f g) h) ->
```
( a
  b
  ( c
    d )
      ( e
        f
        g )
  h )
```

5. Write a FETCH function that receives a key and a list of associations, and if it finds the key it will return only its value. If it does not find it, it will return an appropriate message.
- (fetch 'temperature '((temperature 100) (pressure (120 60)) (pulse 72)))
- 100

6. Write a function that returns a list of all the keys in an association list.

7. Assuming we have symbols that have the father property. Define the grandparent procedure that receives a symbol and returns the paternal grandparent if known, otherwise nil.

8. Define the recursive function ADAM that takes a token and returns the most distant paternal ancestor.

9. Define the recursive function ANCESTORS that returns a list consisting of the person along with all known ancestors, walking on two properties: father and mother.

10. Define a define macro that defines a function with the syntax:
- (define <nume functie> (<param 1> ... <param n>) <corp>)

11. Define a dotimes macro with the syntax:
- (dotimes (<var> <count> <rezultat> <corp>)

The first time <count> is evaluated which must be an integer. Then <var> is successively bound to integers from 0 to the value of <count> minus 1. The body is evaluated each time, and <result> is returned at the end.

12. Write a PRINT-ARRAY function that displays a two-dimensional array received as an argument. Each row of the matrix will be displayed on a new line. Use ARRAY-DIMENSION to find the range of indices.
13. Write a function that transforms an array represented as a list of lists, in both ways shown, into a standard LISP array. Then determine the number of even elements of the matrix.
14. Define a node structure with the elements: root stga dr;

Then implement a function that adds a new node, according to the rule: to the left for values <= than the root, or to the right for values greater than the root. Create a tree.

## Laboratory 5 - OCaml

1. Problem 1 - Write the headoflist and tailoflist functions using the pattern matching mechanism. List.hd or List.tl will not be used.

2. Problem 2 - Write the functions rotate_left and rotate_right that rotate (once) to the left and to the right respectively a list, using match For rotate_left, List.hd , List.tl will not be used, and for rotate-right the function rotate-left is not used.
- Rotate_left: [1;2;3;4] -> [2;3;4;1]
- Rotate_right:[1;2;3;4] -> [4;1;2;3]

3. Problem 3 - Write the functions that insert an element into a tree, search for an element in the tree, and which returns the elements of the tree in unordered and preordered.
