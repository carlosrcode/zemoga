ABOUT THE SOURCE CODE

Solution was compressed into 2 zip files.
SourceCode1.zip and SourceCode2.zip
Unzip both files and put their content in one folder.



FOR RUNNING FROM THE WEB

Web application URL: 	https://blogengine20220301065033.azurewebsites.net/

Web API:		https://blogwebapi20220301.azurewebsites.net/

For retrieving all Approved posts:
https://blogwebapi20220301.azurewebsites.net/api/CustomPost/GetPosts?status=A
For retrieving all posts:
https://blogwebapi20220301.azurewebsites.net/api/CustomPost/GetAllPosts

Please, read the user manual and technical aspects documents for more info.



FOR RUNNING WEB APPLICATION LOCALLY

1. User the SQL Server Management Studio to create an empty database and execute the script blogEngineDBscript.sql
Make sure the script starts with USE <YourDatabaseName>
 
2. Add the roles Editor and Writer by executing:

INSERT INTO ASPNETROLES VALUES(1,'Editor')
INSERT INTO ASPNETROLES VALUES(2,'Writer')

3. Open the solution and update connection string properly in the web config files.

4  Build All.

Also a backup file (BlogEngineDB.bak) is included in case you need to restore database from the same version used during development.


FOR RUNNING WEB APPLICATION USING THE DATABASE DEPLOYED IN AZURE

1. Open the solution and run. Actually solution has been set up to connect to the database deployed in Azure.

SQL Server: 	testdbblog.database.windows.net
user:		mainuser 
password:	4ToTest22


ABOUT CREDENTIALS.

There is a list of credentials in the docuemnt BlogEngineManualUser.pdf, which can be used in the application that is hosted in Azure.
Besides that, it is posible to create new accounts. Email is used as a username and if it starts with letter 'e', the role Editor will be assigned to the account. Otherwise, Writer role will be assigned.

Finally, about estimated time, considering installing software, review some topics, developing, testing, deployment and fixing issues: 28hrs. 
Although topics like Autofac or unit testing were reviewed, it was not possible implemented for a matter of time.