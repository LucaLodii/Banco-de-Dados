### Questão 1)
**Questão 1)** Projetar o primeiro nome e o último nome dos atores de sexo feminino;
```sql
SELECT first_name, last_name 
FROM actors
WHERE gender = 'F';
```

### Questão 2)
**Questão 2)** Projetar o nome dos filmes com ano superior à 1999;
```sql
SELECT name 
FROM movies 
WHERE year > 1999;
```

### Questão 3)
**Questão 3)** Projetar o nome do filme e o nome do diretor de cada filme;
```sql
SELECT movies.name, directors.first_name, directors.last_name
FROM movies
JOIN movies_directors ON movies.id = movies_directors.movie_id
JOIN directors ON movies_directors.director_id = directors.id;
```

### Questão 4)
**Questão 4)** Projetar o nome do filme, nome do actor e o papel que cada ator teve no filme para filmes com ranking acima da nota 6;
```sql
SELECT movies.name, actors.first_name, actors.last_name, roles.role
FROM movies
JOIN roles ON movies.id = roles.movie_id
JOIN actors ON roles.actor_id = actors.id
WHERE movies.rank > 6;
```

### Questão 5)
**Questão 5)** Projetar o nome do diretor e o número de filmes que cada diretor dirigiu;
```sql
SELECT directors.first_name, directors.last_name, COUNT(movies_directors.movie_id) AS qtd_f
FROM directors
JOIN movies_directors ON directors.id = movies_directors.director_id
GROUP BY directors.id, directors.first_name, directors.last_name;
```

### Questão 6)
**Questão 6)** Projetar o gênero e o número de filmes de cada gênero; 
```sql
SELECT genre, COUNT(movie_id) AS qtd_f
FROM movies_genres
GROUP BY genre;
```

### Questão 7)
**Questão 7)** Projetar o gênero, o ranking (nota) médio, mínimo e máximo dos filmes do gênero.
```sql
SELECT movies_genres.genre, AVG(movies.rank) AS med, MIN(movies.rank) AS min, MAX(movies.rank) AS max
FROM movies_genres
JOIN movies ON movies_genres.movie_id = movies.id
GROUP BY movies_genres.genre;
