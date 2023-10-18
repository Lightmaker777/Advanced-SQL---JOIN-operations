## Task 4
<pre>students_db=# SELECT
  mentor.name AS mentor_name,
  student.name AS student_name,
  mentor.city AS mentor_city,
  student.city AS student_city
FROM mentor
LEFT JOIN student ON student.mentor_id = mentor.id
WHERE mentor.city = &apos;Berlin&apos;
OR student.city = &apos;Berlin&apos;
ORDER BY mentor.name;
   mentor_name    |    student_name    | mentor_city | student_city 
------------------+--------------------+-------------+--------------
 Fabienne Martin  | Irmgard Seekircher | Paris       | Berlin
 Julia Vila       | Gerald Hutticher   | Barcelona   | Berlin
 Julius Maxim     | Alex Anjou         | Berlin      | Paris
 Julius Maxim     | Maria Highsmith    | Berlin      | New York
 Melinda O&apos;Connor | Itzi Elizabal      | Berlin      | Barcelona
 Melinda O&apos;Connor | Christian Blanc    | Berlin      | Paris
 Patricia Boulard | Gudrun Schmidt     | Marseille   | Berlin
(7 rows)
</pre>