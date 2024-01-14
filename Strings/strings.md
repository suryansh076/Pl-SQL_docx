# `STRINGS`
## The string in PL/SQL is actually a sequence of characters with an optional size specification
# Examples
```sql
Declare
myName varchar(20):='Suryansh Srivastava';
company varchar(20):='CodedElctrone.net';
choise char:='s';
begin
dbms_output.put_line(myName);
dbms_output.put_line(company);
dbms_output.put_line(choise);
end;
/
```
```sql
--OUTPUT

    Suryansh Srivastava
    CodedElctrone.net
    s


```
# Some Fuctions:
## `Examples`
```sql
DECLARE 
   greetings varchar2(11) := 'hello world'; 
   message varchar2(30) := '......Hello World.....'; 

BEGIN 
   dbms_output.put_line(UPPER(greetings)); 
    
   dbms_output.put_line(LOWER(greetings)); 
    
   dbms_output.put_line(INITCAP(greetings)); 
    
   /* retrieve the first character in the string */ 
   dbms_output.put_line ( SUBSTR (greetings, 1, 1)); 
    
   /* retrieve the last character in the string */ 
   dbms_output.put_line ( SUBSTR (greetings, -1, 1)); 
    
   /* retrieve five characters,  
      starting from the seventh position. */ 
   dbms_output.put_line ( SUBSTR (greetings, 7, 5)); 
    
   /* retrieve the remainder of the string, 
      starting from the second position. */ 
   dbms_output.put_line ( SUBSTR (greetings, 2)); 
     
   /* find the location of the first "e" */ 
   dbms_output.put_line ( INSTR (greetings, 'e')); 

   dbms_output.put_line(RTRIM(message,'.')); 
   dbms_output.put_line(LTRIM(message, '.')); 
   dbms_output.put_line(TRIM( '.' from message)); 
END; 
/ 
```
```sql
--OUTPUT

    HELLO WORLD
    hello world
    Hello World
    h
    d
    world
    ello world
    2
    ......Hello World
    Hello World.....
    Hello World
```