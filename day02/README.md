Data types in golang : 
 
Data type is classification made on type of data.
String -> sequence of characters and is used to represent text.
Numbers which consists of integers and float :
Integers -> Numbers without any decimal part {Whole numbers , 2, 88, 900, -100}
Float -> Numbers with decimal part {3.7, -0.9}
Boolean -> Just 2 values : true and false {0 and 1 are not permitted in go}
Array -> Like list or sequence of element with single data type. {[3, 6, 8, 9] [true, false, true] ["foo", "bar"]}
Slices -> represents a flexible array-like datatype but they also provide more control over memory allocation.
Maps -> collection of key-value pairs. {"x" -> 30 (map of string to integer)}

Why are datatypes needed?
1. categories a set of related values
2. describes the operation that can be done on them.
3. define the way data is stored in the memory.

Memory allocation : whenever we want to store any data in a code a certain amount of memory is allocated to that.
int : 4 or 8 bytes
Boolean: 1 bytes
string: 16 bytes
float: 4 or 8 bytes 


Static and Dynamic typed language:
Static typed language: Languages are said static typed when compiler throws error when we use datatypes incorrectly.{adding 2 numbers and providing 1 and one as input to the addition function throws compiler error}
ex: C, C++, Java.

static typed have better performance, data integrity, bugs can be caught often by compiler.


Dynamically typed language: when datatypes are not enforced by the compiler.{adding 2 numbers and providing 1 and one as input to the addition function does not throws compiler error}
ex: Python, JavaScript, PHP.

dynamically typed is faster to write code, less rigid, shorter learning curve.

Which one is Golang?
Golang is a fast statically typed language and has a concept of types that are either explicitly declared by programmer or implicitly inferred by compiler.


Variables: These are reference to the values.
Keywords : reserved words that have special meaning to the compiler.

Syntax for declaring and assigning value to a variable:
var <variable_name> <data_type> = <value>
ex: 
var s string = "Hello world"
var i int = 43
var b bool = true
var f float64 = 77.04

\n -> newline character {as fmt.Print() method does not print 2 variables on different lines ("\n")}
fmt.Println() -> prints the variables to the new line by default.

Printf -> Format specifiers:
format specifiers tells the golang how to format different kinds of datatypes.
%v -> default format, %d-> integer, %T-> type of value, %c-> used for character, %t-> true or false, %f-> floating point values


Variable declaration :
In go we can also first declare a variable and afterwards assign value to it 
ex :
var user string
user = "harry"

We cannot assign an inapproprite value to a particular variable such as assigning string as 123, compiler will throw an error.

Shorthand way of declaring variables:
variables of same type can be declared on same line and also can be assigned values on the same line.
ex : var s,p string = "hi", "hello"
 
var(
s string = "foo"
i int = 5) 

Short variable decleration: 
s:="Hello world"
Implicitly go have assigned string type to variable s.

Variable scope : 
In golang variable scope is defined using block-
main(){
	inner(){
	}
}

Inner blocks can access variables declared within outer blocks.
But 
Outer blocks cannot access variables that are declared in inner block.


Local vs Global Variables: 
1.Local variables : declared inside a block. These are not accessible outside the block.
2.Global variables: declared outside a block. These are accessible from any part of the program. 

Zero value in golang :
If a variable is declared without assigning any value then it is given default value known as zero value.
zero value depends on datatype of the variable.
bool-> false
int-> 0
float-> 0.0
string-> ""
pointers-> null

Scanner function :
fmt.Scanf("%format_specifier ", &variable)
fmt.Scanf("%s", &name)

fmt.Scanf return 2 values count and err {count -> the no. of args that the function writes to, err-> any error thrown during the execution of the function}

count, err := fmt.Scanf("%s %d", &a, &b)


Finding datatype of a variable:

1. %T format specifier: 
   fmt.Printf("variable grade = %v is of type %T\n", grades, grades)
2. import package "reflect"
   fmt.Printf("Type : %v\n", reflect.TypeOf(100))


Converting one datatype to another :
The process of converting one datatype to another is known as typecasting.
Datatype can be converted in another datatype but this does not guarantee that the value will remain intact.
ex:
var i int = 90
var f float64 = float64(i)


String conversion package (strconv):
1. Itoa()-> converts int to string and returns one value - string formed with given integer.
ex : 
var i int = 42
var s string = strconv.Itoa(i)
fmt.Printf("%q", s)
output -> "42"

2. Atoi()-> converts string to int and returns two values - the corresponding int, error if any.

Constants:
these are the variable whose value once initialized cannot be modified again.
syntax:
const <const_name> <data_type> = <value>

There are 2 types of constants:
1. Typed  
2. Untyped
constants are untyped unless explicitly given a type at declaration. allows much more flexibility.
ex: const age = 12, const h_name, h_age = "harry", 36

constants are typed when we explicitly specify the data type in the declaration. flexibility is lost.
ex: const age int = 12

we can't first declare a const a constant and then initialize a value to it afterwards.
So we have to declare and assign value at the same time.


