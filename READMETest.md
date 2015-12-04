# HTML/CSS Style Guide

## General Style Rules
### Protocol
*Omit the protocol from embedded resources.*

Omit the protocol portion (http:, https:) from URLs pointing to images and other media files, style sheets, and scripts unless the respective files are not available over both protocols.

Omitting the protocol—which makes the URL relative—prevents mixed content issues and results in minor file size savings.

```HTML
<!-- Not recommended -->
<script src="http://www.google.com/js/gweb/analytics/autotrack.js"></script>
```
```HTML
<!-- Recommended -->
<script src="//www.google.com/js/gweb/analytics/autotrack.js"></script>
```
```CSS
/* Not recommended */
.example {
  background: url(http://www.google.com/images/example);
}
```
```CSS
/* Recommended */
.example {
  background: url(//www.google.com/images/example);
}
```


----------------------------------------------------------------
## Basics

### Spaces or tabs.

Use two spaces to indent, no tabs.

### Line lenght

**80**  characters max.

### Whitespace

No trailing whitespace allowed. Clean up after yourself.

### Brackets

Place opening brackets on the same line as the statement.

```c++
if (cool == true) {
  // ok!.
}

if (cool == true)
{
  // Not ok!.
}
```

### Parenthesis

Leave space before and after the parenthesis for `if/while/for/catch/switch/do`

```c++
// consistent.
if (something) {

}

// inconsistent.
if(something){

}
```

### Naming : variables, functions, classes, ...

As C++ standard, use lower case letters. If the name has many words, they must be separated by underscore

```c++
// consistent
int very_cool_name;

// inconsistent.
int BadExample:
```

```c++
// consistent.
class cool_name {

};

// inconsistent.
class ThisIsNotJava {


};
```

### Function Spacing

When executing a function, leave no space between it's name and parens.

```c++
// consistent.
eatIceCream();

// inconsistent.
eatIceCream ();
```

### Return Early

Return early wherever you can to reduce nesting and complexity.

```c++
int some_calculation(int x) {
  if (x < 10)
    return 0;

  int ans = 10;
  /*
    Some logic here
  */
  return ans;
}
```

### One line statements

If a block contains only a single statement it must be placed in a separated line without brackets

```c++
if (something)
  call_superman();
```

### Operators

Unary operators are not separated from the expression in any way:
```c++
counter++;
```

Binary operators should be separated from adjacent expression by spaces:
```c++
int z = x + y;
```


## Other stuff

Under construction


## Cool references

- [ZeroMQ styleguide](http://zeromq.org/docs:style)
- [Google styleguide](http://google-styleguide.googlecode.com/svn/trunk/cppguide.html)
- [Aaron heckmann javascritp styleguide](https://github.com/aheckmann/js-styleguide)
