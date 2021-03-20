# pyAccountManagementSystem
pyAccountManagementSystem is a userfriendly library for adding a very simple and easy to use login system to any application. It uses ![MongoDB](https://www.mongodb.com/) as It's database.

## Installing
Download with ![git](https://git-scm.com/).

```$ git clone https://github.com/mrikea4real/pyAccountManagementSystem```

In the future you will be able to install pyAccountManagementSystem with ![pip](https://pip.pypa.io/en/stable/).

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

## Documentation
The entire system is centered around the _manager_ object. 

```ManagerSetup(Connection string)``` - Creates the account manager, needs the mongodb connection string.

```ManagerClass.login(username,password)``` - Login to an account with username and password.

```ManagerClass.create(username,password,data={})``` - Create an account with username and password, _optionally_ passing along a data json string.

```ManagerClass.get(username)``` - Get data json string from a player.

```ManagerClass.set(username,data)``` - Replace account data with other data.

```ManagerClass.listen(port)``` - Listen on a port for clients to connect. (This should only be used for testing and not in live projects due to It being extremely insecure.

## Contributing
I would be more than happy to accpet contributions. These can come in the form of bug reports, feature requests and pure code!

## Maintainers
* @mrikea4real (Aaron Gotthardsson)
