# mysql
《mysql》 fifth edition

![Image](https://github.com/zhang0xf/mysql5/blob/main/images/cover/mysql5th.PNG)

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

1. `mysql sampdb < create_student.sql -u root -p`**(do firstly as a foreign key)**

2. `mysql sampdb < create_absence.sql -u root -p`

3. `mysql sampdb < create_grade_event.sql -u root -p`

4. `mysql sampdb < create_member.sql -u root -p`

5. `mysql sampdb < create_president.sql -u root -p`

6. `mysql sampdb < create_score.sql -u root -p`

7. **CHECK:**`use sampdb; show tables;`

#### (script files)

* create_absence.sql
* create_grade_event.sql
* create_member.sql
* create_president.sql
* create_score.sql
* create_student.sql

### insert the initial contents of the sampdb database tables:

1. `mysql sampdb < insert_student.sql -u root -p`**(do firstly as a foreign key)**

2. `mysql sampdb < insert_absence.sql -u root -p`

3. `mysql sampdb < insert_grade_event.sql -u root -p`

4. `mysql sampdb < insert_member.sql -u root -p`

5. `mysql sampdb < insert_president.sql -u root -p`

6. `mysql sampdb < insert_score.sql -u root -p`

7. **CHECK:**`select * from absence;`

#### (script files)

* insert_absence.sql
* insert_event.sql
* insert_member.sql
* insert_president.sql
* insert_score.sql
* insert_student.sql

### make sure the tables are in a known state:

1. `mysql -u root -p < init_all_tables.sh sampdb`
