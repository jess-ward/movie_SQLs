# movie_SQLs
15.5 Studio: Movie SQLs
# 1
SELECT title FROM movies;
# 2
SELECT title, year_released FROM movies ORDER BY year_released DESC;
# 3
SELECT * FROM  directors ORDER BY country ASC; 
# 4
SELECT * FROM  directors ORDER BY country ASC, last_name ASC;
# 5
INSERT INTO directors (first_name, last_name, country) VALUES ("Rob", "Reiner", "USA");
COMMIT;
# 6
SELECT last_name, director_id FROM directors WHERE last_name="Reiner";
# 7
INSERT INTO movies (title, year_released, director_id) VALUES ("The Princess Bride", 1987, 11);
# 8 
SELECT title, year_released, last_name FROM movies INNER JOIN directors ON movies.director_id = directors.director_id;
# 9
SELECT title, first_name, last_name FROM directors INNER JOIN movies ON directors.director_id=movies.director_id ORDER BY last_name ASC;
# 10
SELECT first_name, last_name FROM directors INNER JOIN movies ON directors.director_id = movies.director_id WHERE title = "The Incredibles";
# 11
SELECT last_name, country FROM directors INNER JOIN movies ON directors.director_id = movies.director_id WHERE title = "Roma";
# 12
DELETE FROM movies WHERE movie_id = 11;
COMMIT;
# 13
DELETE FROM directors where director_id = 5;

