
* 


```sql
SELECT * FROM table_exercicio

```

* Puedes devolver todas las filas que hacen referencia a dogs? 
[LINK](https://www.sql-easy.com/es/tutorial/#!where_equals)

```sql
SELECT * 
FROM family_members
WHERE species = 'dog';

```

* Can you run return all rows of family members whose num_books_read is greater than 190?
[LINK](https://www.sql-easy.com/es/tutorial/#!where_greater_than)

```sql
SELECT *
FROM family_members
WHERE num_books_read > 190
```

* Can you return all rows in family_members where num_books_read is a value greater or equal to 180?
[LINK](https://www.sql-easy.com/es/tutorial/#!where_greater_than_or_equal)

```sql
SELECT *
FROM family_members
WHERE num_books_read >= 180;
```
