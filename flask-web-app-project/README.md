# flask web application project

## Tasks
1- Create a RESTFUL flask application using json data format.

2- Use CRUD for endpoints.

3- Endpoints are
```
/login
/logout
/user/list
/user/create
/user/delete/{id}
/user/update/{id}
/onlineusers
```

 4- Data
 ```
/user/create
{
  "username": "",
  "firstname": "",
  "middlename": "",
  "lastname": "",
  "birthdate": "",
  "email": "",
  "password": ""
}

/onlineusers
{
  "username": "",
  "ipaddress": "",
  "logindatetime": ""
}
 ```

5- Store data in postgresql.

6- Password should be store salted with sha256.

7- Password complexity should be least [A-Za-z0-9] and min 8 characters.

8- Data should be validates. Example: email format.

9- Log all activities.

10- Serve application using uwsgi and nginx.

### Make it more complicate
Run flask application with more instance using docker.
Create active-active cluster database using bucardo.

