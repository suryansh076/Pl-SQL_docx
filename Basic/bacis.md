# PLSQL

### PL/SQL stands for Procedural Language extensions to the Structured Query Language (SQL). It's a block-structured language that combines SQL with the procedural features of programming languages. PL/SQL is a high-performance, highly integrated database language that performs best with Oracle database server

# Basic Syntax
```sql
DECLARE -- All the Variable and methode should be define here it is OPTIONAL.
   <declarations section> 
BEGIN -- Start Point
   <executable command(s)>
EXCEPTION
   <exception handling> 
END;  -- End Point
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