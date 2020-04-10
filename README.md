# Background - What is Football?

This 44 second clip explains football better than I ever could
https://www.youtube.com/watch?v=nfHOQAT0-Mk

Football is a team sport, 11 players from each team on the field at one time.
Offense attempts to advance the ball by running or passing and the defense attempts to stop the offense.
If you or anyone you know is interested in learning more about football feel free to see the following link
https://en.wikipedia.org/wiki/American_football

Football is the most popular sport in the US, 29 of the 30 most watched television broadcasts in the US were super bowls.
The cost for one - 30 second commercial during the super cost $5.6 million dollars this past year

# How does weather impact the game?

I believe 
![offensive trends](data/

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
