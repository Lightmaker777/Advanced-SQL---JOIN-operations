## Task 5
<pre>students_db=# SELECT
  student.name AS student,
  mentor.city AS city,
  mentor.name AS mentor
FROM student
JOIN mentor ON student.city = mentor.city
ORDER BY mentor.city, student.name, mentor.name;
      student       |   city    |      mentor      
--------------------+-----------+------------------
 Dolores Perez      | Barcelona | Julia Vila
 Emilio Ramiro      | Barcelona | Julia Vila
 Itzi Elizabal      | Barcelona | Julia Vila
 Gerald Hutticher   | Berlin    | Julius Maxim
 Gerald Hutticher   | Berlin    | Melinda O&apos;Connor
 Gudrun Schmidt     | Berlin    | Julius Maxim
 Gudrun Schmidt     | Berlin    | Melinda O&apos;Connor
 Irmgard Seekircher | Berlin    | Julius Maxim
 Irmgard Seekircher | Berlin    | Melinda O&apos;Connor
 Aimaar Abdul       | Chicago   | Laura Wild
 John Goldwin       | Chicago   | Laura Wild
 Maria Highsmith    | New York  | Peter Smith
 Wayne Green        | New York  | Peter Smith
 Alex Anjou         | Paris     | Fabienne Martin
 Christian Blanc    | Paris     | Fabienne Martin
(15 rows)
</pre>