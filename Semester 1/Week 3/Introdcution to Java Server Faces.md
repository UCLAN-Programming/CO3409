# CO3409 Distributed Enterprise Systems 

# Persistence Using a Database and JSFs 



## Summary

This exercise looks at an interface between a JSF frontend and a database. However, the most important parts of the exercise are the use of the IDE to create and populate a database, to generate a class corresponding to a record from the database, and the use of the Java Persistence API to read and write records from Java.

## Purpose

On completion of this you should be able to

1. Use NetBeans to create a database web application
2. Create a simple class from a database using an     object-relational mapping
3. Create and view a database using the NetBeans IDE
4. Load and save entities programmatically

## Activities

This tutorial consists of 4 parts. 

## 1. Creating a Database using the NetBeans IDE

Creating a Database using Netbeans is straightforward. Follow the instructions below. 

1. Run NetBeans. 
   

2. Switch to the Services Pane. 

   

3. Expand the Databases branch. 

   

4. Right-click on the JavaDB leaf. 

   

5. Select Create Database.

   

6. Enter the database name `consult`, and a user `APP` and a password. Make sure that the password you choose is something you can remember! This way you shouldn't forget what it is. If you don't want that kind of responsibility, use `uclan2020`.

   **Note:** *Make sure you use the username `APP`, which is the default database schema. You will have problems if you use another name, because this is used as the schema name. If you get the name wrong, you can create a schema later*.

   

7. Make a note of the name of the Database Location, the folder where you are storing the database (e.g., C:\documents and settings\dgcampbell\.netbeans-derby\consult). [If the IDE complains that the database already exists, navigate to the folder using Windows explorer and delete the consult folder.]. When you click OK, a separate database server application will be started and will create the database for you.

   

8. When the database has been created, a connection node will appear in the Databases branch.

   

9. Right-click on the JavaDB leaf and stop the Server.



### Aside: Using an Embedded Database or a Separate Server

The Derby DBMS can be used as a standalone server or as a library of routines embedded in the application. On a single machine, the embedded server should be slightly less resource hungry. To convert from one to the other, it is a matter of altering the reference to the database folder: it is a URL for the server and a disk path for the embedded library. To access the server, a client library is needed (`derbyclient.jar`); the library for the embedded database is in `derby.jar`. You could change this using the libraries folder in the Projects Tab. 







**![image-20201011133644941](/Users/dan/Library/Application Support/typora-user-images/image-20201011133644941.png)However, if you are using the embedded database in your application, you can't simultaneously access it from NetBeans, so we will stick with the default, a separate database server.**

## 3. Answer the following questions

a)   What is the purpose of JSF?

b)  JSF is a framework. What is a framework?

c)   What is a namespace?

d)  What namespace includes the JSF tags?

e)   How are the JSF tags identified? How could you change this?

f)   What is a POJO?

g)  One of the benefits of using POJOs is that the beans can be reused in other contexts, can the UserNumberBean be easily reused in a different application.

h)  What is the MVC architecture?

i)   In the JSF implementation of the MVC architecture, the controller is the FacesServer. What are the view and the model in the application you've developed?

j)   What is deployment?

k)  What is configuration?

l)   What language is used for configuration files in JEE?

m)  State two ways in which configuration information can be provided in a JSF application.

n)  What is EL?

o)  What property does the JavaBean, UserNumberBean have?

p)  What is a template used for in JSF?

q)  What presentation technology is used for the view in JSF 1? What about JSF 2? What language is used for the latest presentation technology (also known as a view declaration language)?

r)   What is meant by "wiring a bean to a page"?

s)   What is meant by navigation in JSF? How was it done in JSF 1? Outline two ways in which navigation can be specified in JSF 2.

t)   What happens in the validation stage of the JSF request processing lifecycle?

u)  Both the JSP and JSF applications make use of a bean with session scope, what does this mean?

v)  Which of the two implementations is simpler, the JSP or the JSF implementation?

w)  What are the advantages and disadvantages of JSF?

## Additional Reading 

- **The Java EE 7 Tutorial** – Chapter 12: Developing with JavaServer Faces Technology (https://docs.oracle.com/javaee/7/tutorial/jsf-develop.htm (visited 06/10/2017))