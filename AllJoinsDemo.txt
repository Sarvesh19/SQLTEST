SELECT * FROM persons
inner JOIN employee ON persons.personid = employee.id;
+----------+----------+-----------+---------+----------+------+------------+----
------+----------+------------+
| PersonID | LastName | FirstName | Address | City     | id   | name       | sal
ary   | address  | department |
+----------+----------+-----------+---------+----------+------+------------+----
------+----------+------------+
|        2 | pafrvesh | NULL      | NULL    | mumbai   |    2 | parvesh    | 640
00.00 | Katmandu | IT         |
|        3 | musku    | NULL      | NULL    | katmandu |    3 | JayPrakash |  52
20.00 | NULL     | mech       |
|        1 | yadav    | NULL      | NULL    | thane    |    1 | sarvesh    | 145
00.00 | mumbai   | mech       |
+----------+----------+-----------+---------+----------+------+------------+----
------+----------+------------+

SELECT persons.firstname,persons.lastname,employee.name,employee.id FROM persons
inner JOIN employee ON persons.personid = employee.id;

+-----------+----------+------------+------+
| firstname | lastname | name       | id   |
+-----------+----------+------------+------+
| NULL      | pafrvesh | parvesh    |    2 |
| NULL      | musku    | JayPrakash |    3 |
| NULL      | yadav    | sarvesh    |    1 |
+-----------+----------+------------+------+

SELECT * FROM persons

+----------+----------+-----------+---------+----------+
| PersonID | LastName | FirstName | Address | City     |
+----------+----------+-----------+---------+----------+
|        1 | yadav    | NULL      | NULL    | thane    |
|        2 | pafrvesh | NULL      | NULL    | mumbai   |
|        3 | musku    | NULL      | NULL    | katmandu |
|        4 | wf       | NULL      | NULL    |          |
+----------+----------+-----------+---------+----------+

SELECT * FROM employee

+------+------------+----------+----------+------------+
| id   | name       | salary   | address  | department |
+------+------------+----------+----------+------------+
|    2 | parvesh    | 64000.00 | Katmandu | IT         |
|    3 | JayPrakash |  5220.00 | NULL     | mech       |
|    1 | sarvesh    | 14500.00 | mumbai   | mech       |
|    5 | Talathi    | 15744.00 | thane    | instru     |
+------+------------+----------+----------+------------+


SELECT persons.firstname,persons.lastname,employee.name,employee.id FROM persons
 LEFT JOIN employee ON persons.personid = employee.id;
 +-----------+----------+------------+------+
| firstname | lastname | name       | id   |
+-----------+----------+------------+------+
| NULL      | pafrvesh | parvesh    |    2 |
| NULL      | musku    | JayPrakash |    3 |
| NULL      | yadav    | sarvesh    |    1 |
| NULL      | wf       | NULL       | NULL |
+-----------+----------+------------+------+
 
 
 SELECT * FROM persons
 LEFT JOIN employee ON persons.personid = employee.id;

 +----------+----------+-----------+---------+----------+------+------------+----------+----------+------------+

| PersonID | LastName | FirstName | Address | City     | id   | name       | salary   | address  | department |

+----------+----------+-----------+---------+----------+------+------------+----------+----------+------------+

|        2 | pafrvesh | NULL      | NULL    | mumbai   |    2 | parvesh    | 64000.00 | Katmandu | IT         |

|        3 | musku    | NULL      | NULL    | katmandu |    3 | JayPrakash |  5220.00 | NULL     | mech       |

|        1 | yadav    | NULL      | NULL    | thane    |    1 | sarvesh    | 14500.00 | mumbai   | mech       |

|        4 | wf       | NULL      | NULL    |          | NULL | NULL       | NULL | NULL     | NULL       |

+----------+----------+-----------+---------+----------+------+------------+----------+----------+------------+



 SELECT * FROM persons
 right JOIN employee ON persons.personid = employee.id;

 
 +----------+----------+-----------+---------+----------+------+------------+----------+----------+------------+

| PersonID | LastName | FirstName | Address | City     | id   | name       | salary   | address  | department |

+----------+----------+-----------+---------+----------+------+------------+----------+----------+------------+

|        1 | yadav    | NULL      | NULL    | thane    |    1 | sarvesh    | 14500.00 | mumbai   | mech       |

|        2 | pafrvesh | NULL      | NULL    | mumbai   |    2 | parvesh    | 64000.00 | Katmandu | IT         |

|        3 | musku    | NULL      | NULL    | katmandu |    3 | JayPrakash |  5220.00 | NULL     | mech       |

|     NULL | NULL     | NULL      | NULL    | NULL     |    5 | Talathi    | 15744.00 | thane    | instru     |

+----------+----------+-----------+---------+----------+------+------------+----------+----------+------------+
