### Questão 1)
**Questão 1)** Projetar o primeiro nome e o último nome dos atores de sexo feminino;
**R:** A ← σ gender = 'F' (actors)
   π first_name, last_name (A)

---

### Questão 2)
**Questão 2)** Projetar o nome dos filmes com ano superior à 1999;
**R:** A ← σ year > 1999 (movies)
   π name (A)

---

### Questão 3)
**Questão 3)** Projetar o nome do filme e o nome do diretor de cada filme;
**R:** A ← ρ (id_m, name, year, rank) (movies)
   B ← A ⨝ id_m = movie_id (movies_directors)
   C ← B ⨝ director_id = id (directors)
   π name, first_name, last_name (C)

---

### Questão 4)
**Questão 4)** Projetar o nome do filme, nome do ator e o papel que cada actor teve no filme para filmes com ranking acima da nota 6;
**R:** A (id_m, name, year, rank) ← σ rank > 6 (movies)
   B ← A ⨝ id_m = movie_id (roles)
   C ← B ⨝ actor_id = id (actors)
   π name, first_name, last_name, role (C)

---

### Questão 5)
**Questão 5)** Projetar o nome do diretor e o número de filmes que cada diretor dirigiu;
**R:** A (dir_id, qtd_f) ← director_id γ COUNT(movie_id) (movies_directors)
   B ← A ⨝ dir_id = id (directors)
   π first_name, last_name, qtd_f (B)

---

### Questão 6)
**Questão 6)** Projetar o gênero e o número de filmes de cada gênero;
**R:** A (genre, qtd_f) ← genre γ COUNT(movie_id) (movies_genres)
   π genre, qtd_f (A)

---

### Questão 7)
**Questão 7)** Projetar o gênero, o ranking (nota) médio, mínimo e máximo dos filmes do gênero.
**R:** A ← movies ⨝ id = movie_id (movies_genres)
   B (genre, avg, min, max) ← genre γ AVG(rank), MIN(rank), MAX(rank) (A)
   π genre, avg, min, max (B)