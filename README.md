# todo-app-jsp
Web Tech Project
A simple TODO app developed using JSP.
## **Features Implementation**

- Develop User registration module implementation.
- Develop a Login module implementation.
- Develop a Todo CRUD operations implementation.

## **Project Overview**

We built a Todo web application using JSP, Servlet, JDBC and MySQL database and HTML, CSS and JavaScript for frontend.

**Registration**

User Registers using following credentials :

- First Name
- Last Name
- User Name
- Password

**Login**

User Logs In using following credentials :

- User Name
- Password

**Todo List**

Once the user has Registered himself and Logged in then he can keep a Todo list in which he is provided with the following functionalities :

- Users can Add a Task in the Todo list.
- Users can View all Tasks in the Todo list.
- Users can Update a Task in the Todo list.
- Users can Delete a Task in the Todo list.

**Project Structure**

![](https://github.com/13lav/todo-app-jsp/blob/main/screenshots/full.PNG)

**User Registration Module**

1. JavaBean - User.java

JavaBean class which we will use in JSP action tags.

2. Configure JDBC Connection- JDBCUtils.java

Class which contains all JDBC common code.

3. DAO Layer - UserDao.java

Class which contains JDBC code to store User registered data into the users table.

4. Controller Layer - UserController.java

Class to process HTTP request parameters and redirect to the appropriate JSP page after request data stored in the database.

![](https://github.com/13lav/todo-app-jsp/blob/main/screenshots/register.png)

5. View Layer - register.jsp

Common header and footer

- header.jsp
- Footer.jsp

User registration HTML form with the following fields:

- firstName
- lastName
- username
- Password

**User Login Module**

1. JavaBean - LoginBean.java

Class which we used in JSP action tags.

2. DAO Layer - LoginDao.java

Class which contains JDBC code to validate login username and password with users table.

3. Controller Layer - LoginController.java

Class to process HTTP request parameters and redirect to the appropriate JSP page based on the login status. If login is successfully validated with the database then the user is redirected to &quot;todo/todo-list.jsp&quot; page otherwise to login.jsp page.

![](https://github.com/13lav/todo-app-jsp/blob/main/screenshots/login.png)

4. View Layer - login.jsp

HTML form with following fields:

- Username
- Password

**TODO Module**

1. Model Layer - Todo.java

This is a model class representing a Todo entity.

2. DAO Layer

- TodoDao.java
- TodoDaoImpl.java

This DAO class provides CRUD database operations for the table todos in the database.

3. Controller Layer - TodoController

This servlet acts as a page controller for the application, handling all requests from the todo. This TodoController class processes HTTP request parameters and redirects to the appropriate JSP page after requesting data stored in the database:

4. View Layer

![](https://github.com/13lav/todo-app-jsp/blob/main/screenshots/add.png)

- todo-form.jsp

Page to add and edit a todo.

![](https://github.com/13lav/todo-app-jsp/blob/main/screenshots/list_blank.png)

- todo-list.jsp

This page lists out all the todos.

# **Demo/Working**

**User Registration**

![](https://github.com/13lav/todo-app-jsp/blob/main/screenshots/singup__demo.png)

After submitting, the input data is inserted into the database using JDBC connection and the user is redirected to the Login page i.e. login.jsp.

**Login**

![](https://github.com/13lav/todo-app-jsp/blob/main/screenshots/login_demo.png)

At the time of submission of login details, the LoginDao.java containing the JDBC code validates the login username and password with the users table.

**Add new Todo**![](https://github.com/13lav/todo-app-jsp/blob/main/screenshots/add_todo_demo.png)

The save button provides insert data operation for the todo-list table in the database.

**Update Todo**

![](https://github.com/13lav/todo-app-jsp/blob/main/screenshots/add_demo.png)

This page enables the user to use the update operation for the database. The save button first updates the list item data and then gets redirected to the List Todo page.

**List Todo**

![](https://github.com/13lav/todo-app-jsp/blob/main/screenshots/todo_list.png)

Above is the main dashboard for the app displaying the entered tasks fetched from the database and provides options to add, edit or delete a task from the list.

