1. Projetar o primeiro nome e o último nome dos atores de sexo feminino;
    SELECT first_name, last_name 
    FROM actors 
    WHERE gender = 'F';

2. Projetar o nome dos filmes com ano superior à 1999;
    SELECT name
    FROM movies
    WHERE year >= 1999;

3. Projetar o nome do filme e do diretor de cada filme;
