## Task 6
<pre>students_db=# ALTER TABLE student ADD COLUMN local_mentor integer;
ALTER TABLE student ADD CONSTRAINT student_local_mentor_fkey FOREIGN KEY (local_mentor) REFERENCES mentor(id);
ALTER TABLE
ALTER TABLE
students_db=# UPDATE student
SET local_mentor = (
  SELECT mentor.id
  FROM mentor
  WHERE mentor.city = student.city
  LIMIT 1
)
WHERE mentor_id IS NULL;
UPDATE 2
students_db=# SELECT
  id,
  name,
  city,
  mentor_id,
  local_mentor
FROM student
ORDER BY name;
 id |        name        |   city    | mentor_id | local_mentor 
----+--------------------+-----------+-----------+--------------
  3 | Aimaar Abdul       | Chicago   |         1 |             
  9 | Alex Anjou         | Paris     |         3 |             
  8 | Christian Blanc    | Paris     |         4 |             
  1 | Dolores Perez      | Barcelona |         2 |             
 11 | Emilio Ramiro      | Barcelona |           |            6
  5 | Gerald Hutticher   | Berlin    |         6 |             
  4 | Gudrun Schmidt     | Berlin    |         5 |             
  7 | Irmgard Seekircher | Berlin    |         7 |             
  6 | Itzi Elizabal      | Barcelona |         4 |             
 10 | John Goldwin       | Chicago   |         6 |             
  2 | Maria Highsmith    | New York  |         3 |             
 12 | Wayne Green        | New York  |           |            1
(12 rows)
</pre>