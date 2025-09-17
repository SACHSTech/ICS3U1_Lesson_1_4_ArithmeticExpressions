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
```
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
```
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
```
int daysUntilSummer = 180;
daysUntilSummer--;
```

## Other Shortcuts
It is also common to want to modify the current value by adding/subtracting/multiplying/dividing another value.

| Operation | Shortcut |
| --------- | -------- |
| `x = x + y` | `x += y` |
| `x = x - y` | `x -= y` |
| `x = x * y` | `x += y` |
| `x = x / y` | `x /= y` |

## Order of Operation
BEDMAS as you would use in math class applies in code as well. This is the order of operations that applies:
| Parentheses | `()` |
| Multiplication and Division | `*` `/` `%` |
| Addition and Subtraction | `+` `-` |

**NOTE: If there are multiple instances of the same precedence, read left to right**

## Key Notes to Remember with Division
* int / int = int
* int / double = double
* double / int = double
* double / double = double

#### Example 3:
What do you think 5 / 2 is in Java? (if they are both integers)  
Since int / int always results in an integer, it gets truncated (meaning the decimal gets removed)

## Casting
What if we want our int to be a double or your double to be an int?  
We use **casting**, which is turning something of one type into another type.  

To do this, we can add the type we want in between parentheses to cast to that type.  

### Changing `double` to `int`
**Example 4:**
`int x = (int)5.3`
This changes `5.3` into `5`

**Example 5:**
```
// x is a double
double x = 10.3;

// y is now an int with value 10
int y = (int)x;
```
### Changing `int` to `double`
Interestingly the same doesn't apply when attempting to do the same from double to int. This is referred to as **implicit casting**. This is when Java automatically casts the value correctly without the programmer needing to do so. 

**NOTE: Java _will_ cast an int to a double BUT _will NOT_ cast a double to an int**

**Example 6:**
```
// x is in integer
int x = 5;

// y is now a double with value 5.0
double y = x;
```

**Example 7:**
The following example wants to calculate how much money each person gets. However, it results in an _incorrect_ answer:
```
int dollars = 100;
int numOfPeople = 40;
double dollarsPerPerson = dollars / numOfPeople;
```
What do you think the result will be?
<details>
<summary> <b>Answer</b> </summary>
  2.0
</details>

If we cast one of the variables to a double, we'll get the correct result.
```
int dollars = 100;
int numOfPeople = 40;
double dollarsPerPerson = (double)dollars / numOfPeople;
```
