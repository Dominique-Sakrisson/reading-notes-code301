## Visual representation of SQL Joins
 Joins discussed in the article
 - inner JOIN
 - left JOIN
 - right JOIN
 - outer JOIN
 - left excluding JOIN
 - right excluding JOIN
 - outer excluding JOIN
  JOIINS not discussed 
 - cross JOINS
 - self referencingg JOINS
 
 ### inner join
 The simplest most understood join. This returns all records in the left table that have a matching record in the right table;
 ```
 SELECT <select_list> 
FROM Table_A A
INNER JOIN Table_B B
ON A.Key = B.Key
 ```
 
 ### Left Join
 This will return all the records i nthe left table regardless if any of those records have a match in the right table. As well as anything that matches from the 2nd table
 ```
 SELECT <select_list>
FROM Table_A A
LEFT JOIN Table_B B
ON A.Key = B.Key
 ```
 
 ### Right Join
 Returns all records in the right table while returning all those matches from the left table.
 ```
 SELECT <select_list>
FROM Table_A A
RIGHT JOIN Table_B B
ON A.Key = B.Key
 ```
 
 ### Outer Join
 This can be referred to as a full outer join or a full join. This will return all of the records from both tables, it will join matches that happen in either table
 ```
 SELECT <select_list>
FROM Table_A A
FULL OUTER JOIN Table_B B
ON A.Key = B.Key
 ```
 
 ### Left excluding Join
 Will return all records from first table that do not match any records in the right table
 ```
 SELECT <select_list> 
FROM Table_A A
LEFT JOIN Table_B B
ON A.Key = B.Key
WHERE B.Key IS NULL
 ```
 
 ### Right excluding JOin
 This will return al lthe records in table B that do not match any record from table A
 ```
 SELECT <select_list>
FROM Table_A A
RIGHT JOIN Table_B B
ON A.Key = B.Key
WHERE A.Key IS NULL
 ```
 
 ### Outer Excluding Join
 Will return all records from table a that have no match in table b as well as all records in table B that dont have a match in table A
 ```
 SELECT <select_list>
FROM Table_A A
FULL OUTER JOIN Table_B B
ON A.Key = B.Key
WHERE A.Key IS NULL OR B.Key IS NULL
 
 ```
 
 
 
 
 
 
 
 
 
 
 
