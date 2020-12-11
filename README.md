# mysql
《mysql》 fifth edition

[files about "sampdb" which produced by author](http://www.kitebird.com/mysql-book/)

### install database "sampdb":

1. `tar -zxf sampdb.tar.gz`

2. `cd sampdb`

3. **CREATE DATABASE:**`mysql -u root -p < createdb.sql`

4. **ENTER PASSWORD:**

5. **CHECK:**`show databases;`

6. **ADD USER:**`mysql -u root -p < adduser.sql`

7. **CHECK:**`select * from user;`

8. **DELETE USER:**`drop user sampdb@'localhost'`

### create the tables:

* create_absence.sql
* create_grade_event.sql
* create_member.sql
* create_president.sql
* create_score.sql
* create_student.sql

1. **FIRST(As a foreign key to other tables)：**`mysql sampdb < create_student.sql -u root -p`

2. `mysql sampdb < create_absence.sql -u root -p`

3. `mysql sampdb < create_grade_event.sql -u root -p`

4. `mysql sampdb < create_member.sql -u root -p`

5. `mysql sampdb < create_president.sql -u root -p`

6. `mysql sampdb < create_score.sql -u root -p`

7. **CHECK:**`use sampdb; show tables;`

### insert the initial contents of the sampdb database tables:

* insert_absence.sql
* insert_event.sql
* insert_member.sql
* insert_president.sql
* insert_score.sql
* insert_student.sql

1. **FIRST INSERT STUDENT(As a foreign key to other tables):**`mysql sampdb < insert_student.sql -u root -p`

2. `mysql sampdb < insert_absence.sql -u root -p`

3. `mysql sampdb < insert_grade_event.sql -u root -p`

4. `mysql sampdb < insert_member.sql -u root -p`

5. `mysql sampdb < insert_president.sql -u root -p`

6. `mysql sampdb < insert_score.sql -u root -p`

7. **CHECK:**`select * from absence;`

### make sure the tables are in a known state:

1. `mysql -u root -p < init_all_tables.sh sampdb`
