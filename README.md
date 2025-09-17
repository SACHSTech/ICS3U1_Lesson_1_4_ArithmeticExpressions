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

## Key Notes to Remember with Division
* int / int = int
* int / double = double
* double / double = double

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



