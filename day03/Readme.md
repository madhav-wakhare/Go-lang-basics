Operators:
Operators helps us to do mathematical operations on operands.
Comparison operators:
== -> to check if both strings have the same value or not. True if both strings have same value
!= -> True if both string haven't the same value
<,>,<=,>= -> Performed on numbers

Arithmetic operators:
+, -, *, /, %, ++, --
if you use + on string it concatenates 2 strings. "foo" + "bar" -> foobar
but - does not work on strings, it will throw compile time error.

Logical operators:
&&, ||, !

Assignment operators:
=, +=, -=, *=, /=, %=

Bitwise operators:
& -> bitwise AND
| -> bitwise OR
^ -> bitwise XOR
>> -> right shift
<< -> left shift

bitwise AND (&)

• takes two numbers as
operands and does AND
on every bit of two
numbers.

12 = 00001100 (In Binary)
25 = 00011001 (In Binary)
  0 0 0 0 1 1 0 0
& 0 0 0 1 1 0 0 1
________________
0 0 0 0 1 0 0 0 = 8 (In decimal)  

var x, y int = 12, 25
z := x & y
fmt.Println(z)

>>>go run main.go
8
-----------------------------------------------
bitwise XOR (^):

• takes two numbers as
operands and does XOR on
every bit of two numbers

The result of XOR is 1 if the
two bits are opposite.

  0 0 0 0 1 1 0 0
^ 0 0 0 1 1 0 0 1
_________________
0 0 0 1 0 1 0 1 = 21 (In decimal)
--------------------------------------------








