# pirant

[![Build Status](https://travis-ci.org/aayush26/pirant.svg?branch=master)](https://travis-ci.org/aayush26/pirant)
[![Documentation Status](https://readthedocs.org/projects/pirant/badge/?version=latest)](http://pirant.readthedocs.io/en/latest/?badge=latest)
[![Coverage Status](https://coveralls.io/repos/github/aayush26/pirant/badge.svg?branch=master)](https://coveralls.io/github/aayush26/pirant?branch=master)
[![version](https://img.shields.io/pypi/v/pirant.svg)](https://pypi.python.org/pypi/pirant)
[![license](https://img.shields.io/pypi/l/pirant.svg)](https://pypi.python.org/pypi/pirant)
[![GitHub contributors](https://img.shields.io/github/contributors/aayush26/pirant.svg)](https://github.com/aayush26/pirant/graphs/contributors)

devRant API wrapper in Python

```
from pirant import DevRant
devrant = DevRant()

# Get Top 10 Rants
topRants = devrant.get_rants("top", 10, 0)
print topRants['rants'][0]['text']

# Get Recent 10 Rants
recentRants = devrant.get_rants("recent", 10, 0)
print recentRants['rants'][0]['text']

# Get Algo 10 Rants
algoRants = devrant.get_rants("algo", 10, 0)
print algoRants['rants'][0]['text']

# Get Rant and all its comments given Rant Id
rant = devrant.get_rant_by_id(194632)
print rant['rant']['text']
print rant['comments'][0]['body']

# Get Recent 10 weekly (does not accept limit param)
rant = devrant.get_weekly_rants("recent", 10)
print rant['rants'][0]['text']

# Search Rant by keyword
searchResult = devrant.search_rants_by_keyword("devrant")
print searchResult['results'][1]['text']
print searchResult['results'][1]['attached_image']['url']
print searchResult['results'][1]['user_avatar']['i']

```
