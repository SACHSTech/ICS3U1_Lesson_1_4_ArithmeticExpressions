# 1.4 Arithmetic Expressions

Here are some math operators you can use in your equations:  

| Symbol |Operation|
|---|---|
|*| multiplication|
|/| division|
|+ | addition|
|- | subtraction|
|( )| brackets to force order of operations BEDMAS|
|% | modulus - whole number division BUT instead of finding the answer, it finds the remainder.|

## Example 1
```java
class ArithmeticExpressions extends ConsoleProgram {
  
  public void run() {
    
    // Day Age Calculator
    int intAge;
    int intDays;

    intAge = readInt("How old are you? ");
    intDays = intAge * 365;

    System.out.print("You have been alive for this many days: " + intDays);
  }
}
```

## Increment / Decrement
It is very common in programming to want to add one or subtract one to a variable.
There are a couple ways to achieve this:
```java
int counter = 1;
counter = counter + 1;
```
Here, we are adding one to the `counter` variable. In the first line, `counter` is assigned the value `1`. In the next line, it is reassigning the value of `counter` to `2`.

Instead of writing `counter = counter + 1`. There's a shortcut:
`counter++;`

Similarly, we can use the same idea to decrement by 1:
`counter--`

### Example 2
What would be stored in the `daysUntilSummer` variable?
```java
int daysUntilSummer = 180;
daysUntilSummer--;
```

## Other Shortcuts
It is also common to want to modify the current value by adding/subtracting/multiplying/dividing another value.

| Operation | Shortcut |
| --------- | -------- |
| `x = x + y` | `x += y` |
| `x = x - y` | `x -= y` |
| `x = x * y` | `x *= y` |
| `x = x / y` | `x /= y` |

## Order of Operation
BEDMAS as you would use in math class applies in code as well. This is the order of operations that applies:

1. Parentheses `()`
2. Multiplication and Division `*` `/` `%`
3.  Addition and Subtraction `+` `-`

**NOTE: If there are multiple instances of the same precedence, read left to right**

## Key Notes to Remember with Division
* int / int = int
* int / double = double
* double / int = double
* double / double = double

### Example 3
What do you think 5 / 2 is in Java? (if they are both integers)  
Since int / int always results in an integer, it gets truncated (meaning the decimal gets removed)

# Casting

Sometimes we want to change a value from one type to another.  
This process is called **casting**.

We can add the type we want in parentheses to explicitly cast to that type.

## Changing `double` to `int` (explicit casting)

When converting from a larger type to a smaller type (like `double` → `int`), Java does **not** do it automatically because information could be lost.  
You must write the cast yourself. This is called a **narrowing conversion**.

**Example 4**
```java
int x = (int)5.3;   // x becomes 5
```
Notice this **truncates** the decimal, it does *not* round.  

**Example 5**
```java
double x = 10.3;
int y = (int)x;     // y becomes 10
```

## Changing `int` to `double` (implicit casting)

When converting from a smaller type to a larger type (like `int` → `double`), Java does it automatically.  
This is called **implicit casting** or **widening**.

**Example 6 (implicit)**
```java
int x = 5;
double y = x;   // y becomes 5.0
```

You can also write the cast explicitly, though it isn’t required:

**Example 7 (explicit, but optional)**
```java
int x = 5;
double y = (double)x;   // y also becomes 5.0
```

## Casting in Expressions

Casting is especially important in arithmetic expressions.  
Consider this example:

**Example 8 (integer division issue)**
```java
int dollars = 100;
int numOfPeople = 40;
double dollarsPerPerson = dollars / numOfPeople;
```
What do you think the result will be?
<details>
<summary> <b>Answer</b> </summary>
  2.0
</details>

Even though `dollarsPerPerson` is a `double`, the division is done using **integers**, so the result is `2`, stored as `2.0`.

To fix this, we can cast one of the operands to a `double`:

**Example 9 (correct calculation)**
```java
int dollars = 100;
int numOfPeople = 40;
double dollarsPerPerson = (double)dollars / numOfPeople;  // 2.5
```

Now the calculation is done in floating-point arithmetic, giving the correct result.

## Summary Table

| Conversion             | Automatic? | Name                  | Example                       |
|-------------------------|------------|-----------------------|-------------------------------|
| `int` → `double`       | Yes        | Widening (implicit)   | `double y = x;`               |
| `int` → `double`       | Optional   | Explicit cast allowed | `double y = (double)x;`       |
| `double` → `int`       | No         | Narrowing (explicit)  | `int y = (int)z;`             |



Here are some math operators you can use in your equations:  

| Symbol |Operation|
|---|---|
|*| multiplication|
|/| division|
|+ | addition|
|- | subtraction|
|( )| brackets to force order of operations BEDMAS|
|% | modulus - whole number division BUT instead of finding the answer, it finds the remainder.|

## Example 1
```java
class ArithmeticExpressions extends ConsoleProgram {
  
  public void run() {
    
    // Day Age Calculator
    int intAge;
    int intDays;

    intAge = readInt("How old are you? ");
    intDays = intAge * 365;

    System.out.print("You have been alive for this many days: " + intDays);
  }
}
```

## Increment / Decrement
It is very common in programming to want to add one or subtract one to a variable.
There are a couple ways to achieve this:
```java
int counter = 1;
counter = counter + 1;
```
Here, we are adding one to the `counter` variable. In the first line, `counter` is assigned the value `1`. In the next line, it is reassigning the value of `counter` to `2`.

Instead of writing `counter = counter + 1`. There's a shortcut:
`counter++;`

Similarly, we can use the same idea to decrement by 1:
`counter--`

### Example 2:
What would be stored in the `daysUntilSummer` variable?
```java
int daysUntilSummer = 180;
daysUntilSummer--;
```

## Other Shortcuts
It is also common to want to modify the current value by adding/subtracting/multiplying/dividing another value.

| Operation | Shortcut |
| --------- | -------- |
| `x = x + y` | `x += y` |
| `x = x - y` | `x -= y` |
| `x = x * y` | `x *= y` |
| `x = x / y` | `x /= y` |

## Order of Operation
BEDMAS as you would use in math class applies in code as well. This is the order of operations that applies:

1. Parentheses `()`
2. Multiplication and Division `*` `/` `%`
3.  Addition and Subtraction `+` `-`

**NOTE: If there are multiple instances of the same precedence, read left to right**

## Key Notes to Remember with Division
* int / int = int
* int / double = double
* double / int = double
* double / double = double

### Example 3:
What do you think 5 / 2 is in Java? (if they are both integers)  
Since int / int always results in an integer, it gets truncated (meaning the decimal gets removed)

# Casting

Sometimes we want to change a value from one type to another.  
This process is called **casting**.

We can add the type we want in parentheses to explicitly cast to that type.

## Changing `double` to `int` (explicit casting)

When converting from a larger type to a smaller type (like `double` → `int`), Java does **not** do it automatically because information could be lost.  
You must write the cast yourself. This is called a **narrowing conversion**.

**Example 1:**
```java
int x = (int)5.3;   // x becomes 5
```
Notice this **truncates** the decimal, it does *not* round.  

**Example 2:**
```java
double x = 10.3;
int y = (int)x;     // y becomes 10
```

## Changing `int` to `double` (implicit casting)

When converting from a smaller type to a larger type (like `int` → `double`), Java does it automatically.  
This is called **implicit casting** or **widening**.

**Example 3 (implicit):**
```java
int x = 5;
double y = x;   // y becomes 5.0
```

You can also write the cast explicitly, though it isn’t required:

**Example 4 (explicit, but optional):**
```java
int x = 5;
double y = (double)x;   // y also becomes 5.0
```

## Casting in Expressions

Casting is especially important in arithmetic expressions.  
Consider this example:

**Example 5 (integer division issue):**
```java
int dollars = 100;
int numOfPeople = 40;
double dollarsPerPerson = dollars / numOfPeople;
```
What do you think the result will be?
<details>
<summary> <b>Answer</b> </summary>
  2.0
</details>

Even though `dollarsPerPerson` is a `double`, the division is done using **integers**, so the result is `2`, stored as `2.0`.

To fix this, we can cast one of the operands to a `double`:

**Example 6 (correct calculation):**
```java
int dollars = 100;
int numOfPeople = 40;
double dollarsPerPerson = (double)dollars / numOfPeople;  // 2.5
```

Now the calculation is done in floating-point arithmetic, giving the correct result.

## Summary Table

| Conversion             | Automatic? | Name                  | Example                       |
|-------------------------|------------|-----------------------|-------------------------------|
| `int` → `double`       | Yes        | Widening (implicit)   | `double y = x;`               |
| `int` → `double`       | Optional   | Explicit cast allowed | `double y = (double)x;`       |
| `double` → `int`       | No         | Narrowing (explicit)  | `int y = (int)z;`             |
