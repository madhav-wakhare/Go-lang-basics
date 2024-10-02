Golang Installation and Introduction
Docker and Kubernetes (K8S) are written in Golang.  Golang is an open-source programming language supported by Google.

History and Inspiration
Golang was created by engineers at Google to address some of the common issues developers faced in large-scale software development, such as long compilation times and managing dependencies.

What is Golang?
Golang is a compiled programming language, which means the source code you write is translated into machine language that the computer can understand.

Therefore, before we write a Go program, we need a Go compiler.

Installing Go
You can install Go by visiting the official Go installation guide:

https://go.dev/doc/install

This guide provides instructions for various operating systems. Here's an example installation for Ubuntu 22.04:

Extract the Go tar file:
Bash
sudo tar -C /usr/local -xzf go1.23.2.linux-amd64.tar.gz
Use code with caution.

This command extracts the Go binaries to /usr/local/go.

Add /usr/local/go/bin to the PATH environment variable.
(Instructions for adding to PATH vary by operating system. Refer to the official guide for details)

Verify the Go installation:

Bash
go version
Use code with caution.

This should return:

go version go1.23.2 linux/amd64
List all Go commands:
Bash
go help
Use code with caution.

What is a PATH Environment Variable?

The PATH environment variable is a list of directories that the operating system searches to find executable programs.

Your First Go Program
Here's how to write your first "Hello World" program in Go:

Go
package main

import "fmt"

func main() {
  fmt.Println("hello world")
}
Use code with caution.

Explanation:

Package Declaration:

Go
package main
Use code with caution.

Every Go program must start with the package declaration.
Go organizes code using packages. In our case, we're writing an executable program, so we declare main as the package.
Note: The main package is special for programs that are executable, and it contains the main function, which is the entry point of the program.

Importing a Package:

Go
import "fmt"
Use code with caution.

We use the import statement to include code from other packages. The fmt package (short for Format) provides formatting functionalities for input and output.

Function Declaration:

Go
func main() {
Use code with caution.

The main function is special in Go, as it serves as the entry point for every executable program.
There is no need to explicitly call the main function—Go does that automatically when running the program.

Printing to the Console:

Go
fmt.Println("hello world")
Use code with caution.

fmt.Println prints the text "hello world" to the console.
The dot (.) between fmt and Println is a member access operator used to access functions inside the fmt package.

Comments in Go:

Go
// This is a comment
Use code with caution.

Comments are ignored by the compiler and are used to add explanations or notes within the code.


After this we can see a function declaration. Here the name of function is main which is special. We declared main package in first line of code. In go language main package is a special package which is used with programs that are executable and this package contains the main function.
Main function is entry point of the executable programs. So whenever we run a go program go will automatically call the main function.
So there is no need to call the main function explicitly and every executable program must contains single main package and main function.   

An executable program in Go is a computer file that can be run on a computer and contains code written in the Go programming language. 

fmt.println("Hello World") -> the dot between fmt and println is member access operator which helps in accessing the func in the fmt package which is in this case println.

