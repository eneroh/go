# go

## notes
* store the memory address of a value using pointers but disallows pointer arithmatic which causes serious issues
* concurrency with go routines, functions that run at the other time as other functions by utilizing multiple threads on a cpu
* UTF-8 encoding meaning characters outside the vanilla ascii characters are considered 2 characters
* To ensure you get the correct character count for item outside regular ascii characters fmt(printLn(utf8.RuneCountInString("<special symbol>"))
* best practice: be clear with the type
* perform nvim testing by using:
```bash
:! go run <filepath>
```

## operators
```go
!=
```
Not equal comparator

```go
==
```
equal comparator

```go
&&
```
AND, requires both statements to be true

```go
||
```
OR, if true proceed

## syntax
* File must end in .go i.e. hello.go
* File must be compiled using go compiler before running

```go
package main

func main() {

}
```
main layout of go

```go
go build <filename>.go
```
to compile .go

```go
go mod init
go mod init <github repo> [best practice]
```
creates a go module file, which enables dependency tracking
dependency management


```go
var <name> <type> = <value>
var name string = "Jeff"
```
basic variable layout

```go
var
var name string = "John"
```
declare variables

```go
name := "Jeff"
```
Go can auto select type

```go
name, age, likesGo := "John",75, true
```
multiple variable syntax

```go
myArray = [3]string
myArray[0] = "0"
myArray[1] = "1"
myArray[2] = "2"
```
Array layout

```go
myMap = map[string]string
myMap["0"] = "0"
myMap["1"] = "1"
myMap["2"] = "2"
```
Map layout

```go
for x := 0; x < 10; x++ {
  fmt.println("test")
}
```
loop layout

```go
animal := "dog"
if animal == "dog" {
  fmt.println("who's a good boy? YOU ARE!")
} else {
  fmt.println("no dog, sad tiems ):"
}
```
control flow

```go
var year int = 2021;
var p *int = &year
```
pointer layout

```go
uint
```
unsigned integers
Only stores positive integers

```go
int16
```
Only reaches up to 32767, anymore will result in errors

```go
uint8
```
more efficient than int as less bits = more efficient

```go
int
```
int is equivalent to int64

```go
~~var result float32 = floatNum32 + intNum32~~
var result float32 = floatNum32 + float32(intNum32)
```
Convert two different data types to the same to have the correct result

```go
fmt.Println(intNum1/intNum2)
fmt.Println(intNum1%intNum2)
```
/ for whole number
% for float/remainder

```go
var myBoolean bool = false
```
True or false

```go
string
```
default value = ' '

```go
int,uint,float,run
```
default value = 0

```go
bool
```
default value = false

```go
const myConst string = "const value"
```
Cannot change value once created
<br>
Must be given a value, cannot just declare

```go
if err!=nul {
  fmt.Printf(err.Error())
} else if remainder == 0 {
  fmt.Printf("The reuslt of the integer division is %v", result)
} else {
  fmt.Printf("The result of the integer division is %v with remainder %v", result, remainder)
}
```
if statement

```go
switch {
  case err!=nul:
    fmt.Printf(err.Error())
  case remainder==0:
    fmt.Printf("The result of the interger division is %v", result)
  default:
    fmt.Printf("The result of the integer division is %v with remainder %v", result remainder)
}
```
switch statement

## data types
* bool
* float32 float64
* int int16 int32 int64
* rune
* string
* uint uint8 uint16 uint32 uint64

## standard librarys
https://pkg.go.dev/std

## projects

### 1. cli to do list
*functionality*
* tasks add
* tasks list
* tasks complete
* tasks delete

*packages/libs*
* csv
* tabwriter
* timediff
* cobra
* os
* strconv

*Additional functionality*
<br>
--due (due date)

*Sources*
<br>
"Powerful command-line applications in go" by Ricardo Gerardi
<br>
https://github.com/dreamsofcode-io/goprojects/tree/main/01-todo-list

### 2. gui to do list

### 3. web scraper
Scrapes for links on web page for active links.
<br>
Any dead links are logged to console
<br>
Does not work for javascript based websites unless you use headless browser (playwright)
<br>
Will be useful for doing domain enum

### 4. URL shortener

### 5. currency converter utilize open converter api and handle secrets for api key
