# ```For Loop```
## For loop is used when when you want to execute a set of statements for a predetermined number of times
# Syntax:
```sql
FOR counter IN initial_value .. final_value LOOP 

   sequence_of_statements; 

END LOOP;
```
>__Here ```initial_value```  and ```final_value``` both are ```Included``` in Iteration__

# Example:
```sql
Declare
 varInt number(20);
Begin
 for varInt in 0..10 loop
 dbms_output.put_line('Value is  '||varInt);
 end loop;
end;
/
```
```sql
 --OUTPUT

    Value is  0 -->Initial_value
    Value is  1
    Value is  2
    Value is  3
    Value is  4
    Value is  5
    Value is  6
    Value is  7
    Value is  8
    Value is  9
    Value is  10 -->Final_value

```

## Example_2: <sub>```Reverse Order```</sub>
```sql
-- Reverse order Code

for varInt in reverse 0..10 loop
dbms_output.put_line('Reverse Value is ' ||varInt);
end loop;
end;
/
```
```sql
 --OUTPUT

    Reverse Value is 10 -->Final_value
    Reverse Value is 9
    Reverse Value is 8
    Reverse Value is 7
    Reverse Value is 6
    Reverse Value is 5
    Reverse Value is 4
    Reverse Value is 3
    Reverse Value is 2
    Reverse Value is 1
    Reverse Value is 0 -->Initial_value
```
# ```While Loop```

## while loop is used when a set of statements has to be executed as long as a condition is true

# Syntax:
```sql
WHILE condition LOOP 
   sequence_of_statements 
END LOOP;
```
# Example
```sql
Declare
a number(10):=10;
Begin
while a<20 loop
dbms_output.put_line('Value is '||a);
a:=a+1;
end loop;
end;
/

```
```sql
-- OUTPUT

    Value is 10
    Value is 11
    Value is 12
    Value is 13
    Value is 14
    Value is 15
    Value is 16
    Value is 17
    Value is 18
    Value is 19
```