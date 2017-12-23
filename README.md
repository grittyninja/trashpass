[![PyPI version](https://badge.fury.io/py/trashpass.svg)](https://badge.fury.io/py/trashpass)
# Trashpass

Trashpass /ˈtɹɛspəs/ - Library that helps bot developer to read disposable email from [Trash-Mail](https://trash-mail.com)

## Getting Started

### Prerequisites

you need to install prequisites libraries in order to make trashpass run

#### python2
```
pip2 install requests bs4
```

#### python3
```
pip3 install requests bs4
```

### Installing

#### python2
```
pip2 install trashpass
```

#### python3
```
pip3 install trashpass
```

### Testing

this test ensure that you are able to read inbox from dummy email

```
import trashpass

tr = trashpass.Trashpass()

# set disposable email to mysecretinbox1337@trash-mail.com
tr.set_target('mysecretinbox1337')
messages = tr.read_inbox()

# set disposable email to myverysecretinbox1337@trash-mail.com
tr.set_target('myverysecretinbox1337')
messages = tr.read_inbox()

```

## Built With

* [Requests](http://docs.python-requests.org/en/master/) - HTTP Library
* [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) - HTML Parser


## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [0.1.0](https://github.com/hrdn/trashpass/tags). 

## Authors

* **Herdian Nugraha* - *Initial work* - [hrdn](https://github.com/hrdn)


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Thanks to beautifulsoup team for making this project possible