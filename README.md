# go

## notes
* store the memory address of a value using pointers but disallows pointer arithmatic which causes serious issues
* concurrency with go routines, functions that run at the other time as other functions by utilizing multiple threads on a cpu

## syntax
File must end in .go
hello.exe

package main

func main() {

}

to compile .go
```go
go build <filename>.go
```
```go
go mod init 
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
