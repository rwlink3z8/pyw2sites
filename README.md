# pyw2sites

from pymongo import MongoClient
import pprint
import numpy as np
import pandas as pd

# Requests sends and recieves HTTP requests.
import requests

# Beautiful Soup parses HTML documents in python.
from bs4 import BeautifulSoup, Comment
import re
import json
import time

url = 'https://www.pro-football-reference.com/play-index/pgl_finder.cgi?request=1&match=game&year_min=2009&year_max=2019&season_start=1&season_end=-1&pos%5B%5D=QB&is_starter=E&game_type=E&career_game_num_min=1&career_game_num_max=400&qb_start_num_min=1&qb_start_num_max=400&game_num_min=0&game_num_max=99&week_num_min=0&week_num_max=99&c5val=1.0&order_by=pass_td&offset=500'
r = requests.get(url)
type(r)
r.content
pprint.pprint(r.text)

soup = BeautifulSoup(r.text, 'html.parser')

print(soup.prettify())
