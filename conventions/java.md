<div align="center">
  <h1>Unnamed Team Code Conventions</h1>
</div>

## 1. Characters
The files charset is `UTF-8` and it must be specified in the [EditorConfig](https://editorconfig.org/) `.editorconfig` file.
The end of line must be `LF`, and must also be specified in `.editorconfig` file.

## 2. Source Structure
The member order by accessibility is `public`, `protected`, package-private and then `private`.
Method overloading is an exception, they must always appear together.

The source code files order must be:
- License or header (optional)
- Package specification (`package team.unnamed.example;`)
- Import statements (`import team.unnamed.example.ExampleClass;`)
- Class definition (`class ExampleClass {...`)
- Static fields
- Instance fields
- Static Initializer Block
- Instance Initializer Block
- Constructors
- Methods (Should be grouped by functionality rather than by accessibility. The goal is to make understandable code)

## 3. Braces
Braces are always used in `if`, `else`, `for`, `while` and `do` statements. Lambda expressions can omit the braces, i.e. `() -> value`

## 4. Line Breaks
It's very important to use only one line per statement.
`something(); somethingElse();` isn't accepted.

### 4.1 Some restrictions
- A comma should not be separated from the word that precedes it.
```java
void doSomething(
    Example param
    , Example param2 // <--- Bad!
) {

}
```

- A lambda arrow (`->`) should not be separated from its parameters.
```java
Consumer<Thing> consumer = thing -> // <--- Ok!
    {...};

consumer = thing // <--- Bad!
  -> {...};
```

## 5. Whitespace and Empty Lines
There must be exactly one whitespace or a line break if necessary within `if`, `else`, `do`, `while`, `for` and `(`/`{`
