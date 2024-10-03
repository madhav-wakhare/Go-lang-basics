Data Types in Golang
What is a Data Type?
A data type is a classification of data, describing how the data is used and stored. Each data type has its own set of operations that can be performed on it.

Basic Data Types:
String: A sequence of characters used to represent text.

Example: "Hello World"
Numbers: Consists of integers and floating-point numbers.

Integers: Numbers without a decimal part.
Example: 2, 88, 900, -100
Float: Numbers with a decimal part.
Example: 3.7, -0.9
Boolean: Represents one of two values: true or false.

Note: Go does not permit 0 and 1 for Boolean values.
Example: true, false
Array: A fixed-size sequence of elements of a single data type.

Example: [3, 6, 8, 9], [true, false, true], ["foo", "bar"]
Slices: A flexible, array-like data type that provides more control over memory allocation.

Example: []int{3, 5, 7}
Maps: A collection of key-value pairs.

Example: map[string]int{"x": 30} (A map of strings to integers)
Why are Data Types Needed?
Categorize a set of related values.
Describe the operations that can be performed on them.
Define how the data is stored in memory.
Memory Allocation:
Each data type requires a certain amount of memory for storage:

int: 4 or 8 bytes (depending on architecture)
bool: 1 byte
string: 16 bytes
float: 4 or 8 bytes
Static and Dynamic Typing:
Static Typed Languages:
Definition: Languages in which the compiler enforces correct usage of data types at compile time.
Example: Adding two numbers but providing incorrect types (e.g., "one" + 1) will result in a compile-time error.
Examples: C, C++, Java.
Advantages:
Better performance.
Improved data integrity.
Bugs can often be caught by the compiler.
Dynamic Typed Languages:
Definition: Languages in which the data types are not enforced by the compiler.

Example: In dynamically typed languages, adding "one" + 1 would not throw a compiler error.

Examples: Python, JavaScript, PHP.
Advantages:

Faster to write code.
More flexible.
Easier to learn, shorter learning curve.
Golang's Typing System:
Go is a fast, statically typed language. It requires data types to be either explicitly declared or inferred by the compiler.

Variables in Golang:
Syntax:
A variable is a reference to a value. Here's how to declare and assign values to variables:

go
Copy code
var <variable_name> <data_type> = <value>
Examples:

go
Copy code
var s string = "Hello world"
var i int = 43
var b bool = true
var f float64 = 77.04
Shorthand Variable Declaration:
You can declare and assign a variable in a single line using shorthand syntax:

go
Copy code
s := "Hello world"
Implicitly, Go assigns the correct data type based on the value.

Multiple Variable Declaration:
You can declare multiple variables on the same line:

go
Copy code
var s, p string = "hi", "hello"
You can also declare multiple variables within a block:

go
Copy code
var (
  s string = "foo"
  i int = 5
)
Variable Scope:
In Go, variable scope is defined by the block in which the variable is declared:

go
Copy code
func main() {
    // outer block
    func inner() {
        // inner block
    }
}
Variables in inner blocks can access variables from outer blocks.
Variables in outer blocks cannot access variables from inner blocks.
Local vs Global Variables:
Local Variables: Declared inside a block. These are not accessible outside the block.
Global Variables: Declared outside a block. These are accessible from any part of the program.
Zero Value in Golang:
When a variable is declared without an initial value, Go assigns it a zero value based on the data type:

bool: false
int: 0
float: 0.0
string: ""
pointers: nil
Input Handling with Scanner Function:
The fmt.Scanf function reads formatted input:

go
Copy code
fmt.Scanf("%format_specifier", &variable)
Examples:

go
Copy code
fmt.Scanf("%s", &name)
count, err := fmt.Scanf("%s %d", &a, &b)
count: Number of arguments written to.
err: Any errors during execution.
Type Information:
1. %T Format Specifier:
To find the data type of a variable, use %T:

go
Copy code
fmt.Printf("variable = %v is of type %T\n", grades, grades)
2. Using reflect Package:
To find the type of a variable at runtime:

go
Copy code
fmt.Printf("Type : %v\n", reflect.TypeOf(100))
Type Conversion:
Typecasting is the process of converting one data type into another:

go
Copy code
var i int = 90
var f float64 = float64(i)
String Conversion:
Go provides the strconv package to convert between strings and other data types.

strconv.Itoa(): Converts an int to a string.

go
Copy code
var i int = 42
var s string = strconv.Itoa(i)
fmt.Printf("%q", s)  // Output: "42"
strconv.Atoi(): Converts a string to an int.

go
Copy code
var s string = "42"
var i int, err = strconv.Atoi(s)
Constants:
A constant is a variable whose value cannot be changed after initialization.

Syntax:
go
Copy code
const <const_name> <data_type> = <value>
Examples:

go
Copy code
const age = 12
const h_name, h_age = "harry", 36
Typed vs Untyped Constants:
Untyped Constants: Do not have an explicit type unless assigned one.
Typed Constants: Have a specific type assigned during declaration.
Example:

go
Copy code
const age int = 12
Note: Constants must be initialized at the time of declaration. You cannot declare a constant and assign its value later.
