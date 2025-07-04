# Project-Three-Solution
Download Here: [Project Three Solution](https://programming.engineering/product/cnt-4714-project-three-solution/)

Objectives: To develop a two-tier Java based client-server application interacting with a MySQL database utilizing JDBC for the connectivity. This project is designed to give you some experience using the various features of JDBC and its interaction with a MySQL DB Server environment.

Description: In this assignment you will develop a Java-based GUI front-end (client-side) application that will connect to your MySQL server via JDBC.

You are to develop a Java application that will allow any client (the end-user) to execute commands against the database. You will create a Java GUI-based application front -end that will accept any MySQL DDL or DML command, pass this through a JDBC connection to the MySQL database server, execute the statement and return the results to the client. Note that while technically your application must be able to handle any DDL or DML command, we won’t actually use all of the commands available in these sublanguages. For one thing, it would be quite rare to allow a client to create a database or a table within a database. Note too, that the only DML command that uses the executeQuery() method of JDBC is the Select command, all other DML and DDL commands utilize executeUpdate(). Some screen shots of what your Java GUI front -end should look like are shown below. Basically, this GUI is an extension of the GUI that was developed in the lecture notes and is available on WebCourses as DisplayQueryResults.java. Your Java application must give the user the ability to execute any SQL DDL or DML command for which the user has the correct permissions. Note also, that if the user wishes to change databases in the middle of a session, they must reconnect to the new database. Their user information can remain in the proper window, but you must click the reconnect button to establish a connection to the new database. You do not need to support simultaneous connections from your application to more than one database in this assignment. However, you will be able to start multiple instances of your Java application and allow different clients to connect simultaneously to the MySQL server, since the default number of connections is set at 151 (see your Workbench options file under the networking tab).

Once you’ve created your application, you will execute a sequence of DML and DDL commands and illustrate the output from each in your GUI for two different users. For this project you will create, in addition to the root user, a client user with limited permissions on the database (see below). The root user is assumed to have all permissions on the database, any command they issue will be executed. The client user will be far more restricted.

References for this assignment:
Notes: Lecture Notes for MySQL and JDBC.

Input Specification:
The first step in this assignment is to login to the MySQL Workbench as the root user and execute/run the script to create and populate the backend database. This script is available on the assignment page and is named “project3dbscript.sql”. This script creates a database named project3. You can use the MySQL Workbench for this step, or the command line whichever you prefer.

Page 1
The second step is to create authorizations for a client user (in addition to the root user) named client. By default your root user has all permissions on the project3 database. Use either SQL Grant statements from the command line or the MySQL Workbench (see separate document for details on how to accomplish this task) to check and set permissions for the client as follows:

Register the new user named client (assign them the password client – ignore the MySQL warning on weak password setting) and assign to this user only selection privileges on the project3 schema.

Output Specification: There are two parts for the output for this project. Part 1 is to provide screen shots from your application which clearly show the complete query/command expression and results for each of the commands that appear in the script named: project3rootuserscript.sql available on the course website. There are eight different commands in this script and some of the commands will have more than one output capture (see below). Part 2 is to provide screen shots from your application which clearly show the complete query/command expression and results for each of the commands that appear in the script named: project3clientuserscript.sql available on the course website. There are three different commands in this script and some of the commands will have more than one output capture (see below). To produce your final output, first recreate the database, then run the root user commands followed by the client commands.

Deliverables:
Zip up all of the .java files associated with your application as well as the screen shots from each of the commands specified in both the project3rootuserscript.sql and project3clientuserscript.sql files via WebCourses no later than 


Details:
Shown below is a screen shot of the initial GUI. Notice that there are drop-down lists for selecting the JDBC driver and database URL that the client must select. The client must also specify a username and password (MySQL option) before connecting to the database.

You should provide buttons for the user to clear the command window as well as the result window.
The status of the connection should be returned to the GUI and displayed in the connection area.

The output of all SQL commands should be returned to the SQL Execution Result window. Please note that only SQL commands can be executed via this application, we will not go to the effort of making the application display the results of MySQL-specific commands. (When a MySQL-specific command is executed, the SQL Execution Result window does not need to display any results, if you wanted to you could display the line “MySQL command executed” in the results window, but this is not required.)


Note that for non-query DML and DDL commands, before and after screen shots must be taken to illustrate the basic effect of the command. See pages 8-9 for an illustration of this.


