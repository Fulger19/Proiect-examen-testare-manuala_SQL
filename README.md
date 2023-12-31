# Proiect-examen-testare-manuala_SQL

The scope of the final project for ITF Manual Testing Course is to use all gained knowledge about SQL and aplly them in practice, using a live application.

Under test: a database for the students in the 8th grade

Tools used: MySQL Workbench

## Testing section

### 1.1 DDL instructions (create, alter, delete, drop)

### 1.1.1 Create and use database (first step)

The first step was to create and use a database for a school. 

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/7e09fb25-3b62-4be3-acce-139ae0b86010)

### 1.1.2 Create tables

First, I created a table with the children in a specific grade.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/a593db9b-a723-4fb8-a86c-0f84df5ca199)

Then, I created a table with the average grades of the children for two subjects (mathematics and romanian language) in order to know their situation.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/099de63f-dd4a-4a25-8b08-f073496765de)

Another table created was with employees of two schools (teachers, directors, cleaning personnel)

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/01c4422f-d0e1-4f10-b664-8da6788a0ada)

And then a table with schools, where the column id_director had a foreign key referencing the employees table and the id_employee column in the previous table. 

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/53dfc86b-091f-446d-80a5-352229d495db)

I also created two tables for specific subjects (mathematics and french). For mathematics I added 3 grades for each child, using also the child_id so that a later stage I could have an average for each child using this child_id.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/72afa968-0f9e-49e1-9b91-1fcbbb86d23f)

For french_grades table I add 3 grades as 3 separate columns. 

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/5dfdb1d9-9b33-400e-85eb-2075474c2337)


### 1.1.3 Alter table

I altered the table with the averages for romanian and mathematics, adding a foreign key to connect it with the table with the children in the 8th grade (copii8C). I also tested if the drop request functioned. 

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/d48a6435-a429-4abb-be8a-d5bec617477f)

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/37d81a48-6ba1-44b9-9a8b-97ea28f20605)

Then I altered the table subjects, renaming some columns.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/bf18a794-a08a-48e8-867c-3fe9709ec23f)

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/f83740b7-7f4a-4f5b-bccd-5251e5ad3eb9)

I altered the table for the french_grades to add a column for the average, which later I updated.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/8135a991-aa74-4532-a1b2-f333c388e303)


### 1.1.4 Drop table

I used the drop table function for the schools table.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/8441110d-54a8-4c9d-a78e-0b2b8a8bcf92)

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/487ae394-7485-426d-844a-f9b001df0174)


### 1.2 DML instructions (insert, update, delete)

### 1.2.1 Insert data in table

I added data in the table copii8C, with personal information about children.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/48264c71-38d7-4ac7-9bd6-365fb94d3225)

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/3c1623a2-37ae-4cfc-aac1-e43ff4c63fec)

I also populated the schools and employees tables.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/4063db9a-5c95-408b-a124-2fa9abd49978)

For the employees table I used two types of inserting information, as shown below.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/0b1d8a98-dfb4-4210-a5ae-6547676e2d33)


### 1.2.2 Update data in a table

I updated the table note8C to add the "pass/failed" inputs for each student in the column situation.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/ede906d3-44b9-4fdd-b8c3-8429f8731949)

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/95610725-4c5e-4fdb-b712-43d81257e836)

I updated the french_grades table to include the average of the 3 grades and I also altered the datatype to decimals to reflect the correct average. 

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/fba47c52-ed72-4c1d-ad90-79b9c70d4bab)


### 1.3 DQL instructions (simple select, select with filters, select using the AND, NOT, OR, LIKE operators, agregated functions)

### 1.3.1 Selecting

For the table copii8C I used a series of selections with filters on sex or birth year. 

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/a3bc3aba-8077-4fa5-abb0-4400ba8ddc12)

For the table note8C I used a series of selections with filters on the grades for mathematics, romanian or both subject. 

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/b129d8a8-8ce8-4dff-857d-c93c4c061434)

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/3e62c70c-2c1f-4885-ade3-adfcc328917a)

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/230ea062-892d-48c9-9c3d-dfe72b56a8b7)

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/8175fd06-5082-4ced-a30b-be256288454d)

For the french_grades table I used the select instruction to find out the average for each child

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/fbc597c9-b2d6-461b-9e05-d34a3a30da3f)

### 1.3.2 AND and OR operators

I updated the table note8C with the situation of the students (pass or failed) using the AND and OR operators.

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/ba303ae5-2761-403e-acc8-353d155a5d87)

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/40d8a61e-29b5-4adb-8f43-66288482e0d8)


When using the AND operator, the table only returns the students with both grades under 5. 

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/718d7242-78c4-4d80-afff-18f97906a6f5)

When using the OR opertor, the table returns all the students that have at least one grade under 5. A student is considered passed if they have both grades equal or above 5. 

![image](https://github.com/Fulger19/Proiect-examen-testare-manuala_SQL/assets/135150028/429f8131-b67a-47ac-8c13-82afea9fb068)
