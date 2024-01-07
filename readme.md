# PLSQL

### PL/SQL stands for Procedural Language extensions to the Structured Query Language (SQL). It's a block-structured language that combines SQL with the procedural features of programming languages. PL/SQL is a high-performance, highly integrated database language that performs best with Oracle database server

# Basic Syntax
```sql
DECLARE -- All the Variable and methode should be define here it is OPTIONAL.
   <declarations section> 
BEGIN -- Start Point
   <executable command(s)>
EXCEPTION  -- End Point
   <exception handling> 
END;
```
## Exmaple :-

```sql
DECLARE 
   message  varchar2(20):= 'Hello, World!'; 
BEGIN 
   dbms_output.put_line(message); 
END; 
/ 
```
OUTPUT 
```Console```
```md
Hello World

PL/SQL procedure successfully completed.
```

# Data Types
![Alt text](image.png)

# Variables <sub>Declaration and Assigning</sub>
```sql
declare

 -- Variable Initialization 

  a integer;
  b integer;
  c integer;

 -- Assigning value to variables

 myname varchar(100):='Suryansh';
 varint number:=500;
 mydate date:=sysdate;
begin
  dbms_output.put_line(myname);
  dbms_output.put_line(varint+15);
  dbms_output.put_line(mydate);
end;
/

OUTPUT: 

    Suryansh
    515
    01/07/2024
    
Statement processed.

0.01 seconds

```
# Delimaters : ```important```

 ![Alt text](image-1.png)