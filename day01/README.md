Docker and K8S are written in golang.
Golang is a open-source programming language supported by google.
History and inspiration behind developing golang -
created by engineer in google.

golang is a compiled programming language which means the source code you have written is translated into a language that the computer can understand.
Therefore before we write a go program we need a go compiler.

One can install go by simply visiting -> https://go.dev/doc/install

I have ubuntu 22.04 : 
I have downloaded tar file : go1.23.2.linux-amd64.tar.gz
1. sudo tar -C /usr/local -xzf go1.23.2.linux-amd64.tar.gz (to extract the GO binaries to /usr/local/go)
2. Add /usr/local/go/bin to the PATH environment variable.
3. Now check the go version by -> go version
go version go1.23.2 linux/amd64 

go help -> all go commands are listed 

*What is a PATH env variable?
The PATH environment variable is a list of directories that an operating system searches to find executable programs.


here is the first go program to write a hello world :

package main

import "fmt"

func main() {
    fmt.Println("hello world")
}

Here package is the go's way of organizing and reusing the code.
Every go program must start with the package declaration.
When you will build reusable pieces of code then you will develop a package as a shared library.
But in our case we would be developing executable programs.

Next line is import 'fmt' -> we use import statement to include code from other packages to use with our program.
Fmt package is short form of Format and it implements formatting for input and output. we are importing this because we need functionalities provided by this package.
Also the package name is surrounded by double quotes "".

Comment // {Comments are ignored by compilers and interpreters}

After this we can see a function declaration. Here the name of function is main which is special. We declared main package in first line of code. In go language main package is a special package which is used with programs that are executable and this package contains the main function.
Main function is entry point of the executable programs. So whenever we run a go program go will automatically call the main function.
So there is no need to call the main function explicitly and every executable program must contains single main package and main function.   

An executable program in Go is a computer file that can be run on a computer and contains code written in the Go programming language. 

fmt.println("Hello World") -> the dot between fmt and println is member access operator which helps in accessing the func in the fmt package which is in this case println.
