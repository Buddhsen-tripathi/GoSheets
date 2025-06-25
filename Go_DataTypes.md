# Go Built-in Data Types Cheat Sheet

##  Boolean
```go
var b bool = true
```
- Values: ```true```, ```false```  
- Size: 1 byte

## Integer Types

| Type     | Size     | Range                            |
|----------|----------|----------------------------------|
| ```int```    | 4/8 bytes| Depends on architecture          |
| ```int8```   | 1 byte   | -128 to 127                      |
| ```int16```  | 2 bytes  | -32,768 to 32,767                |
| ```int32```  | 4 bytes  | -2,147,483,648 to 2,147,483,647  |
| ```int64```  | 8 bytes  | -9.2 quintillion to +9.2 quint.  |
| ```uint8```  | 1 byte   | 0 to 255                         |
| ```uint16``` | 2 bytes  | 0 to 65,535                      |
| ```uint32``` | 4 bytes  | 0 to 4.2 billion                 |
| ```uint64``` | 8 bytes  | 0 to 18 quintillion              |

- ```byte``` = alias for ```uint8```  
- ```rune``` = alias for ```int32``` (for Unicode characters)

## Floating Point
```go
var x float64 = 3.14
```

| Type       | Precision         |
|------------|-------------------|
| ```float32``` | ~6 decimal places |
| ```float64``` | ~15 decimal places (default) |

## Complex Numbers
```go
var c complex64 = 2 + 3i
```
- ```complex64``` = ```float32``` real + imaginary  
- ```complex128``` = ```float64``` real + imaginary

## String
```go
s := "hello"
fmt.Println(s[0]) // byte access
```
- UTF-8 encoded  
- Immutable  
- Use ```[]rune(s)``` to handle Unicode characters properly

## Arrays
```go
var arr [3]int = [3]int{1, 2, 3}
```
- Fixed size  
- Type + size are part of definition

## Slices
```go
s := []int{1, 2, 3}
s = append(s, 4)
```
- Dynamic, resizable  
- More commonly used than arrays

## Maps
```m := map[string]int{"a": 1, "b": 2}```
- Key-value pairs  
- Keys must be comparable

## Structs
```go
type Person struct {
    name string
    age  int
}
```

```go
p := Person{name: "Gopher", age: 10}
fmt.Println(p.name)
```
- Like objects (without inheritance)  
- Used to group fields

## Pointers
```go
x := 10
p := &x
fmt.Println(*p)
```
- Store memory addresses  
- No pointer arithmetic

## Special Types
- ```interface{}``` — can hold any value  
- ```error``` — built-in interface for error handling  

```var err error = errors.New("something went wrong")```
