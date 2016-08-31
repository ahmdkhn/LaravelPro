# LaravelPro
A small Laravel application that highlights some of the components of a typical Laravel project.


**Application Description**  

This application is a small user management system, which provides functionalities as follows:
* Multiple groups can be created.
* Groups can also be updated, and deleted. 
* Multiple users can be created, where each user can be part of any number of groups, initially he can be part of three groups.

To make each of the funcitonality clear, group creation, deletion, and editing is provided separately. However, many of the features can be combined in a single form and according to the actions of a user deifferent actions can be performed. A user after entering valid password and username can edit all the details related to him, as well as in the next step he  can also view the groups which are related to him. The application makes use of Laravel's  Eloquent ORM while manipulating data available in MysQl DB. 

**Implementation Details**

The underlying structure of the application consists of User, Group, User-Group Model which are manipulated through a single controller named as AdminController. As it is a small application, therefore, the logic to manipulate models is placed inside AdminController, however, for large applications it is recommended to follow the repository and service design patterns. As it makes logic quite easier to manage when it is placed in separate repositories and data required in multiple places can be placed inside a service. Using Laravel's builtin Authentication controller a user is registered first, and then he/she will be be able to get into the system. 

At the time of user registrtaion and inside the system all the passwords are created/edited and managed in the database using Laravel's Bcrypt hashing scheme. This scheme uses a new salt every time, and thus, each time even if we use the same password, the scheme generates a different hashed password. 

**Installation Details**  

Clone the repository unzip it and in the LaravelPro folder there is a MySQL_Dump folder which contains a demo.sql file required to re-create the database. An Http Server is also required to run the application. 
