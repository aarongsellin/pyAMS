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
```

_Create Ex_:
```
>>> from pyAccountManagementSystem import *
>>> manager = ManagerSetup("mongodb://mongodb0.example.com:27017")
>>> manager.create("username","password")
1
```

## Documentation

## Contributing
I would be more than happy to accpet contributions. These can come in the form of bug reports, feature requests and pure code!

## Maintainers
* @mrikea4real (Aaron Gotthardsson)
