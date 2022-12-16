
# Guia básico de SQL

Alvaro J. Lopez


Uma forma muito legal de aprender SQL é praticando. O site https://www.sql-easy.com/ nos ensina de uma forma interativa a usar os comandos SQL mais úteis. Para praticar nesse site são propostos exercícios SQL.

Assim neste post eu soluciono todos os problemas de SQL apresentados no site https://www.sql-easy.com/.

O objetivo é que este post serva como uma ajuda para todos aqueles que desejam mergulhar no SQL de uma forma simples e (bem) prática. 


### SELECT *

* Devolver todas as colunas da tabela. [LINK](https://www.sql-easy.com/es/tutorial/#!select)


```sql
SELECT *
FROM family_members
```

### SELECT

* ¿Puedes devolver sólo las columnas name y species? [LINK](https://www.sql-easy.com/es/tutorial/#!select_columns)

```sql
SELECT name, species
FROM family_members
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

* Can you find all of Pickles' friends that are dogs and under the height of 45cm?

[LINK](https://www.sql-easy.com/es/tutorial/#!and)

```sql
SELECT * 
FROM friends_of_pickles
WHERE species = 'dog' AND height_cm < 45
```

* Can you find all of Pickles' friends that are dogs or under the height of 45cm?
[LINK](https://www.sql-easy.com/es/tutorial/#!or)

```sql
SELECT * 
FROM friends_of_pickles
WHERE species = 'dog' OR height_cm < 45;
```

* Can you run a query that would return the rows that are not cats or dogs?
[LINK](https://www.sql-easy.com/es/tutorial/#!in)

```sql
SELECT * 
FROM friends_of_pickles
WHERE species NOT IN ('cat', 'dog')
```

* Can you return a list of the distinct species of animals greater than 50cm in height?
[LINK](https://www.sql-easy.com/es/tutorial/#!distinct)

```sql
SELECT DISTINCT species 
FROM friends_of_pickles
WHERE height_cm > 50
```

* Can you run a query that sorts the friends_of_pickles by height_cm in descending order?
[LINK](https://www.sql-easy.com/es/tutorial/#!order_by)


```sql
SELECT * 
FROM friends_of_pickles
ORDER BY height_cm DESC
```

### LIMIT

* Can you return the single row (and all columns) of the tallest friends_of_pickles?


```sql
SELECT * 
FROM friends_of_pickles
ORDER BY height_cm DESC LIMIT 1
```

### COUNT

*  returns the total number of rows in the table friends_of_pickles
```sql
SELECT COUNT(*) 
FROM friends_of_pickles
```