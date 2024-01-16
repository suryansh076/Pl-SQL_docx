# Arrays
## __A collection of items of the same data type stored in a contiguous fashion. In PL/SQL A `VARRAY` is created with `CREATE TYPE `. This is a part of `'PL/SQL Collections'`__
# Syntax:

```sql
TYPE varray_type_name IS VARRAY(n) of <element_type>
```
# Example - 1:

```sql
Declare
Type String_array is varray(5) of varchar2(20);
name_array String_array;
len_count number(10);
Begin
name_array:=String_array('Surynash','Sushant','Chitransh','Amit','Harsh');
len_count:=name_array.count;
for i in 1..len_count loop
dbms_output.put_line('Value is '||name_array(i));
end loop;
end;
/
```
```sql
-- OUTPUT

    Value is Surynash
    Value is Sushant
    Value is Chitransh
    Value is Amit
    Value is Harsh
```
# Example - 2:
```sql
Declare
Type Int_array is varray(5) of number(10);
num_array int_array;
len_count number(10);
Begin
num_array:=int_array(19,31,17,14,07);
len_count:=num_array.count;
for i in 1..len_count loop
dbms_output.put_line('Value is '||num_array(i));
end loop;
end;
/
```
```sql
-- OUTPUT

    Value is 19
    Value is 31
    Value is 17
    Value is 14
    Value is 7
```