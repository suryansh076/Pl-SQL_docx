# Procedures
## __Procedures is also names as PL/SQL Block that accepts some input in the form of parameter and perform some task and may or may not return a value.`Used for repeated execution`.__

# Syntax
```sql
CREATE OR REPLACE PROCEDURE <procedure_name>(Parameter if any) 
{IS | AS} 

BEGIN 
  < procedure_body > 
END procedure_name; 
```
# Type of Parameter
There are 3 types;
# 1. `IN` --> Default 
## It always receive the value send by the Caller

# 2. `OUT`
## It always send the value 
# 3. `IN OUT`
## Sends as well as receive the values

![Alt text](image.png)

# __In Oracle PL/SQL, there are two common ways to define procedures__
# 1. _Define Procedure within DECLARE Block_:
* ##  This approach is used when you want to define a procedure that is local to the current PL/SQL block.
*  ## The procedure is declared and defined within the DECLARE block itself, and it is only accessible within that block.

```sql
DECLARE 
   a number; 
   b number; 
   c number;
PROCEDURE findMin(x IN number, y IN number, z OUT number) IS 
BEGIN                                     
   IF x < y THEN 
      z:= x; 
   ELSE 
      z:= y; 
   END IF; 
END;   
BEGIN 
   a:= 23; 
   b:= 45; 
   findMin(a, b, c); 
   dbms_output.put_line(' Minimum of (23, 45) : ' || c); 
END; 
/
```
> ## Here in given example `Z` is declared  as `OUT` so whatever value it will contain, passed back to the calling block through the `Z` parameter. In the calling block, the variable `C` is used to receive the result.
```sql
 --OUTPUT

    Minimum of (23, 45) : 23

    Statement processed.

```
# 2. CREATE OR REPLACE PROCEDURE Statement: 
* ## This approach -is used when you want to create a standalone procedure that can be stored in the database for future use _`or in a separate file`_.
* ## The `CREATE OR REPLACE PROCEDURE` statement is used to define the procedure, and it can be stored in the database for repeated execution.
```SQl
CREATE OR REPLACE PROCEDURE doMul(x IN NUMBER, y IN NUMBER) IS
  c NUMBER;
BEGIN
  c := x * y;
  dbms_output.put_line('Multiplication is ' || c);
END doMul;
/
-- OUTPUT

  Procedure created.

  0.01 seconds

--> Here a new procedure is created as doMul
```
  
>## To call this procedure we have 2 ways
## 1. `write anonymous block`
### Now we can open any/new `Work sheet` and can call this procedure
```sql
DECLARE
  a NUMBER := 10;
  b NUMBER := 20;
BEGIN
  doMul(a, b);
END;
/
```
```sql
--OUTPUT

  Multiplication is 200

  Statement processed.

```
## 2. Using `EXECUTE` Command