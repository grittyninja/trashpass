# Trashpass
[![PyPI version](https://badge.fury.io/py/trashpass.svg)](https://badge.fury.io/py/trashpass)

Trashpass /ˈtɹɛspəs/ - Library that helps bot developer to read disposable email from [Trash-Mail](https://trash-mail.com)

## Getting Started

### Prerequisites

you need to install prequisites libraries in order to make trashpass run

```
pip install requests bs4
```

### Installing

```
pip install trashpass
```

### Testing

this test ensure that you are able to read inbox from dummy email

```
import trashpass

tr = trashpass.Trashpass()

""" set disposable email to mysecretinbox1337@trash-mail.com """

tr.target('mysecretinbox1337')
messages = tr.read()


""" set disposable email to myverysecretinbox1337@trash-mail.com """

tr.target('myverysecretinbox1337')
messages = tr.read()
# messages = {}


""" refresh inbox """

tr.refresh()
messages = tr.read()
# messages = {'2': {'from': 'dummysend@gmail.com', 'subject': 'Re: this is test box email', 'date': '23.12.2017 - 8:07 am', 'text': 'hallo  '}, '1': {'from': 'dummysend@gmail.com', 'subject': 'this is test box email', 'date': '23.12.2017 - 8:05 am', 'text': 'halo  '}}

"" get session """
session = tr.session
# session = {'PHPSESSID': 'g24hq61gv6d9gnckck316f65u6'}

```

## Built With

* [Requests](http://docs.python-requests.org/en/master/) - HTTP Library
* [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) - HTML Parser


## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [1.1](https://github.com/hrdn/trashpass/tags). 

## Authors

* **Herdian Nugraha** ([hrdn](https://github.com/hrdn))


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Thanks to beautifulsoup team for making this project possible
