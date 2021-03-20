# pyAMS
pyAMS stands for _Account management system_ and is a userfriendly library for adding a very simple and easy to use login system to any application. It uses ![MongoDB](https://www.mongodb.com/) as It's database.

## Installing
Download with ![git](https://git-scm.com/).

```$ git clone https://github.com/mrikea4real/pyAMS```

In the future you will be able to install pyAMS with ![pip](https://pip.pypa.io/en/stable/).

## Examples
_Login Ex_:
```
>>> from pyAccountManagementSystem import *
>>> manager = ManagerSetup("mongodb://mongodb0.example.com:27017")
>>> manager.login("username","password")
1
``````

_Create Ex_:
```
>>> from pyAccountManagementSystem import *
>>> manager = ManagerSetup("mongodb://mongodb0.example.com:27017")
>>> manager.create("username","password")
1
```

_Client Login Ex_:
```
>>> import socket
>>> 
>>> loginStr = {"login":{"username":"tester","password":"password"}}
>>> s = socket.socket()
>>> 
>>> s.connect((10.10.10.10,8500))
>>> s.send(bytes(loginStr,encoding="ASCII"))
>>> print(str(s.recv(1024),encoding="ASCII"))
Logged in.
>>> s.close()
```

_Client Create Ex_:
```
>>> import socket
>>> 
>>> createStr = {"create":{"username":"tester","password":"password","data":{"name":"John Doe"}}}
>>> s = socket.socket()
>>> 
>>> s.connect((10.10.10.10,8500))
>>> s.send(bytes(createStr,encoding="ASCII"))
>>> print(str(s.recv(1024),encoding="ASCII"))
Account created.
>>> s.close()
```

## Documentation
The entire system is centered around the _manager_ object. 

```ManagerSetup(Connection string)``` - Returns the account manager, needs the mongodb connection string.

```ManagerClass.login(username,password)``` - Login to an account with username and password.

```ManagerClass.create(username,password,data={})``` - Create an account with username and password, _optionally_ passing along a data json string.

```ManagerClass.get(username)``` - Returns account data in json string format.

```ManagerClass.set(username,data)``` - Replace account data with other data.

```ManagerClass.listen(port)``` - Listen on a and handle client logins. (This should **not** be used in live projects, only for testing)

## Contributing
I would be more than happy to accpet contributions. These can come in the form of bug reports, feature requests and pure code!

## Maintainers
* @mrikea4real (Aaron Gotthardsson)
