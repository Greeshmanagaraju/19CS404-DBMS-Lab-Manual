# Experiment 7: PL/SQL – Variables, Control Structures and Loops

## AIM
To write and execute simple PL/SQL programs using variables, loops, and conditional statements.


## THEORY

PL/SQL, which stands for Procedural Language extensions to the Structured Query Language (SQL). It is a combination of SQL along with the procedural features of programming languages.

**Syntax:**
```sql
DECLARE 
   <declarations section> 
BEGIN 
   <executable command(s)>
EXCEPTION 
   <exception handling> 
END;
```

### Basic Components of PL/SQL Block:
- DECLARE: Section to declare variables and constants.
- BEGIN: The execution section that contains PL/SQL statements.
- EXCEPTION: Handles errors or exceptions that occur in the program.
- END: Marks the end of the PL/SQL block.

# PL/SQL Programs – Steps and Expected Output

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

### Steps:
- Declare two numeric variables and initialize them.
- Use an `IF` statement to compare the values.
- Display the greater number using `DBMS_OUTPUT.PUT_LINE`.
```
DECLARE
    a NUMBER :=&a;
    b NUMBER :=&b;

BEGIN
    IF a > b THEN
        DBMS_OUTPUT.PUT_LINE('Greatest number is: ' || a);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Greatest number is: ' || b);
    END IF;
END;
/
```
**Expected Output:**  
Greater number is: 80
<img width="914" height="674" alt="image" src="https://github.com/user-attachments/assets/fa5be983-0e6d-4790-a3a2-30df6a00ae36" />


---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.
```
DECLARE
    n NUMBER := 10;
    i NUMBER := 1;
    total NUMBER := 0;

BEGIN
    WHILE i <= n LOOP
        total := total + i;
        i := i + 1;
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Sum of first ' || n ||
    ' natural numbers is: ' || total);
END;
/
```
**Expected Output:**  
Sum of first 10 natural numbers is: 55

<img width="940" height="665" alt="image" src="https://github.com/user-attachments/assets/0e684912-e201-426e-b781-6a570681faf5" />

---

## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.
 ```
  DECLARE
    n NUMBER := 7;
    a NUMBER := 0;
    b NUMBER := 1;
    c NUMBER;
BEGIN
    DBMS_OUTPUT.PUT_LINE('Fibonacci sequence:');

    FOR i IN 1..n LOOP
        DBMS_OUTPUT.PUT(a || ' ');

        c := a + b;
        a := b;
        b := c;
    END LOOP;

    DBMS_OUTPUT.NEW_LINE;
END;
/
```


**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8

<img width="961" height="682" alt="image" src="https://github.com/user-attachments/assets/5ee1cf62-1b5b-47c8-a593-5e2bd5d33cf3" />

## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

**Expected Output:**  
n = 1535  
Reversed number is 5351

---

## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15

## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.
