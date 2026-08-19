# Experiment 7: PL/SQL – Variables, Control Structures and Loops

## NAME : SANTHOSH KUMAR A
## REG NO: 212224230250



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

### Program:

```
DECLARE
    a NUMBER := 80;
    b NUMBER := 40;
BEGIN
    IF a > b THEN
        DBMS_OUTPUT.PUT_LINE('Greatest number is: ' || a);
    ELSIF b > a THEN
        DBMS_OUTPUT.PUT_LINE('Greatest number is: ' || b);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Both numbers are equal');
    END IF;
END;
/
```

**Expected Output:**  
Greater number is: 80
<img width="965" height="908" alt="Screenshot 2026-08-19 133953" src="https://github.com/user-attachments/assets/e9a67a8f-88fd-4957-bef9-f7f9019b4c4f" />

---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.


## Program:

```
DECLARE
    n NUMBER := 10;
    sum NUMBER := 0;
BEGIN
    FOR i IN 1..n LOOP
        sum := sum + i;
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Sum of first ' || n || ' natural numbers is: ' || sum);
END;
/
```


**Expected Output:**  
Sum of first 10 natural numbers is: 55
<img width="1109" height="931" alt="Screenshot 2026-08-19 134348" src="https://github.com/user-attachments/assets/d510de05-3f64-44de-8fbc-99979976e142" />

---

## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

### Program:
```
DECLARE
    n NUMBER := 7;
    a NUMBER := 0;
    b NUMBER := 1;
    c NUMBER;
BEGIN
    DBMS_OUTPUT.PUT_LINE('Fibonacci Series:');

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


<img width="1103" height="928" alt="Screenshot 2026-08-19 134604" src="https://github.com/user-attachments/assets/5cce1f86-acac-4940-af70-3ce9067cd832" />



---

## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

### Program:
```
DECLARE
    n NUMBER := 1535;
    rev NUMBER := 0;
    rem NUMBER;
BEGIN
    WHILE n > 0 LOOP
        rem := MOD(n, 10);
        rev := rev * 10 + rem;
        n := TRUNC(n / 10);
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Reverse number is: ' || rev);
END;
/

```
**Expected Output:**  
n = 1535  
Reversed number is 5351
<img width="1119" height="937" alt="Screenshot 2026-08-19 134912" src="https://github.com/user-attachments/assets/a0136366-b4ce-4605-b429-ebf754dd3e71" />

---

## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.
### Program:
```
DECLARE
    a NUMBER := 10;
    b NUMBER := 9;
    c NUMBER := 15;
    largest NUMBER;
BEGIN
    IF a > b AND a > c THEN
        largest := a;
    ELSIF b > a AND b > c THEN
        largest := b;
    ELSE
        largest := c;
    END IF;

    DBMS_OUTPUT.PUT_LINE('Largest number is: ' || largest);
END;
/

```
**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15

<img width="1045" height="891" alt="Screenshot 2026-08-19 135118" src="https://github.com/user-attachments/assets/1bc52630-add9-4b91-b8d7-cdc58a8f4461" />



## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.
