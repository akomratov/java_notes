# Types in Java



## Primitive types

Non-numeric types:
* boolean
* char - 2 Bytes


Numeric types:
* byte - 1 Byte
* short - 2 Bytes
* int - 4 Bytes
* long - 8 Bytes
* float
* double

## String
String is `immutable`.

`\` - escape character


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
* `append(), insert(), replase(), delete()`
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
Methods of StringBuffer marked as `synchronized` for use in multithreaded applications.

