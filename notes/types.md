# Types in Java
* [Primitive types](#primitive-types)
* [String](#string)
  - [Formatting strings](#formatting-strings)

## Primitive types

**8 primitive** types:

* Non-numeric types and corresponding Wrapper classes (`immutable`):
  - `boolean` (`true`, `false`) - 1 Byte (`Boolean`)
  - `char` - 2 Bytes (`Character`)


* Numeric types:
  - `byte` - 1 Byte (`Byte`)
  - `short` - 2 Bytes (`Short`)
  - `int` - 4 Bytes (`Integer`)
  - `long` - 8 Bytes (`Long`)
  - `float` - (`Float`)
  - `double` - (`Double`)


`Autoboxing` and `unboxing` when primitive type var used with var of wrapper class.


## String
String is `immutable`.

`\` - escape character

### Formatting strings
`String.format()` specifiers:
* `%s` - String
* `%d` - byte, short, int, long
* `%f` - double, float
* `%b` - boolean
* `%c` - char
* `%t` - Date
* `%%` - `%` chanracter

```java
String str = String.format("a=%3$d, b=%2$d, c=%d", c, b, a);
```

### String Pool
Internal area for storing String literals (`deduplication`).

Method `String.intern()` returns reference to String in String Pool.
```java
String s1 = new String("String literal");
String s2 = new String("String literal");
String comparison = String.format("s1 == s2: %b. s1.intern() == s2.intern(): %b", 
    s1 == s2, s1.intern() == s2.intern());
System.out.println(comparison);

Output:
s1 == s2: false. s1.intern() == s2.intern(): true
```

### StringTokenizer
```java
String str = "Alice, Bob, Carol, David";

StringTokenizer tokenizer = new StringTokenizer(str,", ");
while (tokenizer.hasMoreTokens())
{
   String token = tokenizer.nextToken();
   System.out.println(token);
}
```

### StringBuilder
`StringBuilder is mutable`, it is to be used to overcome String immutable nature.

Popular methods:
* `append(), insert(), replace(), delete()`
* `charAt(), setCharAt(), deleteCharAt()`
* `substring(), reverse()`
* `indexOf(), lastIndexOf()`
* `length()`
* `toString()`

```java
String str = new StringBuilder("Hello world!")
    .replace(6,11, "Universe")
    .toString();
```

### StringBuffer
Similar to `StringBuilder`, methods of `StringBuffer` marked as `synchronized` for use in multithreaded applications.

