```python
%load_ext sql
```


```python
%sql sqlite://
```


```sql
%%sql
create table emp1 (name  varchar(50), roll number varchar(50));
insert into emp1 values('komal', 'rd21');
insert into emp1 values('karan', 'rd22');
select * from emp1;
```

     * sqlite://
    Done.
    1 rows affected.
    1 rows affected.
    Done.
    




<table>
    <tr>
        <th>name</th>
        <th>roll</th>
    </tr>
    <tr>
        <td>komal</td>
        <td>rd21</td>
    </tr>
    <tr>
        <td>karan</td>
        <td>rd22</td>
    </tr>
</table>



# Constraints 


```sql
%%sql
create table emp2 (Reg_no number(10) PRIMARY KEY, Name  varchar(50) NOT NULL, roll number varchar(50) UNIQUE);

```

     * sqlite://
    (sqlite3.OperationalError) table emp2 already exists
    [SQL: create table emp2 (Reg_no number(10) PRIMARY KEY, Name  varchar(50) NOT NULL, roll number varchar(50) UNIQUE);]
    (Background on this error at: https://sqlalche.me/e/14/e3q8)
    

# inserting data


```sql
%%sql
insert into emp2 values(12105221, 'karan', 'Rd2111A29');

```

     * sqlite://
    1 rows affected.
    




    []



# view data


```sql
%%sql
select * from emp2;
```

     * sqlite://
    Done.
    




<table>
    <tr>
        <th>Reg_no</th>
        <th>Name</th>
        <th>roll</th>
    </tr>
    <tr>
        <td>12105221</td>
        <td>karan</td>
        <td>Rd2111A29</td>
    </tr>
</table>




```sql
%%sql
insert into emp2 values(12107402, 'komal', 'Rd2111A49');
```

     * sqlite://
    1 rows affected.
    




    []




```sql
%%sql
select * from emp2;
```

     * sqlite://
    Done.
    




<table>
    <tr>
        <th>Reg_no</th>
        <th>Name</th>
        <th>roll</th>
    </tr>
    <tr>
        <td>12105221</td>
        <td>karan</td>
        <td>Rd2111A29</td>
    </tr>
    <tr>
        <td>12107402</td>
        <td>komal</td>
        <td>Rd2111A49</td>
    </tr>
</table>




```sql
%%sql
insert into emp2 values(12107423, 'komal', 'Rd211150');
insert into emp2 values(1210703, 'komal', 'Rd211A45');
insert into emp2 values(1210404, 'komal', 'R2111A47');
insert into emp2 values(1217405, 'komal', 'd2111A90');
insert into emp2 values(1207406, 'komal', 'R111A09');
insert into emp2 values(1107407, 'komal', 'R11A19');


```

     * sqlite://
    1 rows affected.
    1 rows affected.
    1 rows affected.
    1 rows affected.
    1 rows affected.
    1 rows affected.
    




    []



# use of where clause 


```sql
%%sql
select * from emp2 where name= 'komal';

```

     * sqlite://
    Done.
    




<table>
    <tr>
        <th>Reg_no</th>
        <th>Name</th>
        <th>roll</th>
    </tr>
    <tr>
        <td>12107402</td>
        <td>komal</td>
        <td>Rd2111A49</td>
    </tr>
    <tr>
        <td>12107409</td>
        <td>komal</td>
        <td>Rd2111A50</td>
    </tr>
    <tr>
        <td>12107403</td>
        <td>komal</td>
        <td>Rd2111A45</td>
    </tr>
    <tr>
        <td>12107404</td>
        <td>komal</td>
        <td>Rd2111A47</td>
    </tr>
    <tr>
        <td>12107405</td>
        <td>komal</td>
        <td>Rd2111A90</td>
    </tr>
    <tr>
        <td>12107406</td>
        <td>komal</td>
        <td>Rd2111A09</td>
    </tr>
    <tr>
        <td>12107407</td>
        <td>komal</td>
        <td>Rd2111A19</td>
    </tr>
</table>




```sql
%%sql
select * from emp2;
```

     * sqlite://
    Done.
    




<table>
    <tr>
        <th>Reg_no</th>
        <th>Name</th>
        <th>roll</th>
    </tr>
    <tr>
        <td>12105221</td>
        <td>karan</td>
        <td>Rd2111A29</td>
    </tr>
    <tr>
        <td>12107402</td>
        <td>komal</td>
        <td>Rd2111A49</td>
    </tr>
    <tr>
        <td>12107409</td>
        <td>komal</td>
        <td>Rd2111A50</td>
    </tr>
    <tr>
        <td>12107403</td>
        <td>komal</td>
        <td>Rd2111A45</td>
    </tr>
    <tr>
        <td>12107404</td>
        <td>komal</td>
        <td>Rd2111A47</td>
    </tr>
    <tr>
        <td>12107405</td>
        <td>komal</td>
        <td>Rd2111A90</td>
    </tr>
    <tr>
        <td>12107406</td>
        <td>komal</td>
        <td>Rd2111A09</td>
    </tr>
    <tr>
        <td>12107407</td>
        <td>komal</td>
        <td>Rd2111A19</td>
    </tr>
    <tr>
        <td>12107423</td>
        <td>komal</td>
        <td>Rd211150</td>
    </tr>
    <tr>
        <td>1210703</td>
        <td>komal</td>
        <td>Rd211A45</td>
    </tr>
    <tr>
        <td>1210404</td>
        <td>komal</td>
        <td>R2111A47</td>
    </tr>
    <tr>
        <td>1217405</td>
        <td>komal</td>
        <td>d2111A90</td>
    </tr>
    <tr>
        <td>1207406</td>
        <td>komal</td>
        <td>R111A09</td>
    </tr>
    <tr>
        <td>1107407</td>
        <td>komal</td>
        <td>R11A19</td>
    </tr>
</table>


