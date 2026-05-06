### Questão 1)
**Questão 1)** Projetar o primeiro nome e o último nome dos atores que são diretores;
```sql
SELECT first_name, last_name FROM actors
INTERSECT
SELECT first_name, last_name FROM directors;
```

### Questão 2)
**Questão 2)** Projetar o primeiro nome e o último nome dos atores que não são diretores;
```sql
SELECT first_name, last_name FROM actors
EXCEPT
SELECT first_name, last_name FROM directors;
```

### Questão 3)
**Questão 3)** Projetar o primeiro nome e o último nome dos atores e diretores;
```sql
SELECT first_name, last_name FROM actors
UNION
SELECT first_name, last_name FROM directors;
```

### Questão 4)
**Questão 4)** Projetar o nome dos filmes que não são dirigidos por nenhum diretor;
```sql
SELECT movies.name
FROM (
    SELECT id FROM movies
    EXCEPT
    SELECT movie_id FROM movies_directors
) AS RES
JOIN movies ON RES.id = movies.id;
```

### Questão 5)
**Questão 5)** Projetar primeiro nome e o último nome dos atores que não atuaram em pelo menos dois filmes;
```sql
SELECT actors.first_name, actors.last_name
FROM (
    SELECT id FROM actors
    EXCEPT
    SELECT actor_id FROM roles
    GROUP BY actor_id
    HAVING COUNT(movie_id) >= 2 
) AS RES
JOIN actors ON RES.id = actors.id;
```

### Questão 6)
**Questão 6)** Projetar, por gênero e ano, o número médio de filmes com menos de dois atores atuando.
```sql
SELECT movies_genres.genre, movies.year, COUNT(RES.id) AS qtd_f
FROM (
    SELECT id FROM movies
    EXCEPT
    SELECT movie_id FROM roles
    GROUP BY movie_id
    HAVING COUNT(actor_id) >= 2 
) AS RES
JOIN movies ON RES.id = movies.id
JOIN movies_genres ON RES.id = movies_genres.movie_id
GROUP BY movies_genres.genre, movies.year;
```