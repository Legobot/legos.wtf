# Wikipedia Top Finder

[![Travis](https://img.shields.io/travis/bbriggs/legos.wtf.svg)]() [![PyPI](https://img.shields.io/pypi/pyversions/legos.wtf.svg)]() [![PyPI](https://img.shields.io/pypi/v/legos.wtf.svg)]()

[![PyPI](https://img.shields.io/pypi/wheel/legos.wtf.svg)]() [![PyPI](https://img.shields.io/pypi/l/legos.wtf.svg)]() [![PyPI](https://img.shields.io/pypi/status/legos.wtf.svg)]()

Ever wish you could do an "I'm feeling lucky" search on Wikipedia right from chat? Want to be able to pull up a wikipedia link right there in the group and settle the debate once and for all? This module will search the English langauge Wikipedia for the query you provide and return the URL for the top matching page. 

## Usage

This lego listens for `!wtf` at the beginning of a message and processes everything after it as a query. 

Example: `!wtf python` will return https://en.wikipedia.org/wiki/Python

## Installation

`pip3 install legos.wtf`

This is a Lego designed for use with [Legobot](https://github.com/bbriggs/Legobot), so you'll get Legobot along with this. To deploy it, import the package and add it to the active legos like so:

```python
# This is the legobot stuff
from Legobot import Lego
# This is your lego
from legos.wtf import WikipediaTopFinder

# Legobot stuff here
lock = threading.Lock()
baseplate = Lego.start(None, lock)
baseplate_proxy = baseplate.proxy()

# Add your lego
baseplate_proxy.add_child(WikipediaTopFinder)
```

## Tweaking

While you can use this one as-is, you could also add a localized version to your Legobot deployment by grabbing [wtf.py](legos/wtf.py) and deploying is as a local module. [Example of a Legobot instance with local modules](https://github.com/voxpupuli/thevoxfox/)

## Contributing

As always, pull requests are welcome.
