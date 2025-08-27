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

    System.out.print("You have been alive for this many days: ");
    System.out.println(intDays);
  }
}
```

## Key Notes to Remember with Division
* int / int = int
* int / double = double
* double / double = double


