## Task 2
<pre>students_db=# SELECT
  s.name AS student_name,
  COALESCE(m.name, NULL) AS mentor_name,
  s.city AS student_city,
  COALESCE(m.city, NULL) AS mentor_city
FROM student s
LEFT JOIN mentor m ON s.mentor_id = m.id
ORDER BY s.name;
    student_name    |   mentor_name    | student_city | mentor_city 
--------------------+------------------+--------------+-------------
 Aimaar Abdul       | Peter Smith      | Chicago      | New York
 Alex Anjou         | Julius Maxim     | Paris        | Berlin
 Christian Blanc    | Melinda O&apos;Connor | Paris        | Berlin
 Dolores Perez      | Laura Wild       | Barcelona    | Chicago
 Emilio Ramiro      |                  | Barcelona    | 
 Gerald Hutticher   | Julia Vila       | Berlin       | Barcelona
 Gudrun Schmidt     | Patricia Boulard | Berlin       | Marseille
 Irmgard Seekircher | Fabienne Martin  | Berlin       | Paris
 Itzi Elizabal      | Melinda O&apos;Connor | Barcelona    | Berlin
 John Goldwin       | Julia Vila       | Chicago      | Barcelona
 Maria Highsmith    | Julius Maxim     | New York     | Berlin
 Wayne Green        |                  | New York     | 
(12 rows)</pre>