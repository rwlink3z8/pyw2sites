# Background - Rain and the passing game

I chose this topic because it was interesting to me, I played football through college and anecdotally,
I always believed the greatest impact inclement weather had on the game could be seen in the passing game.
I find it interesting because the greatest evolution over time has been a fundamental shift towards a pass first offense.

![offensive trends](https://github.com/rwlink3z8/pyw2sites/blob/master/images/eldo5-rushing-and-passing-yards-per-team-game_1.png)

that image came from:
https://www.eldo.co/nfl-rushing-and-passing-in-four-charts.html


# Hypothesis - Inclement weather in the form of rain or snow has a negative impact on the passing game

How to test this?

I found the passing statistics from all regular season and post season games on the website:
https://www.pro-football-reference.com/

and through previous work I linked the game stats with the weather data from the website:
http://nflweather.com/

# EDA 
After linking the two dataframes the total games in my dataset were 1330.
I put weather into 4 categories:
Bad weather - 75 games fell into this category: the focus here was on rain and snow
Good weather - 951 games 
Dome - 238 games fell into this category
Unknown - 66 games fell into this category, these are largely Chargers and Rams games, I need to go back to my code
          and see why it did that, I believe it occured when I was cleaning the data due to both teams moving cities
          
I compared bad weather conditions first to games played in domes:

![bad weather v dome](https://github.com/rwlink3z8/pyw2sites/blob/master/images/dome%20v%20bad%20weather%20passing%20yard%20comparison.png)

Next I compared inclement weather conditions to other games played outdoors:
![bad weather v outside](https://github.com/rwlink3z8/pyw2sites/blob/master/images/Passing%20yard%20distributions%20outdoor%20games%20good%20v%20bad%20weather.png)

I also compared the passing yards for outdoor games in good weather and games played in domes:

![good weather v dome](https://github.com/rwlink3z8/pyw2sites/blob/master/images/Domes%20and%20Good%20weather%20passing%20yard%20distributions.png)



NFL stats can be scraped somewhat painlessly from 
pro-football-reference.com
For this capstone weather data was scraped from
nflweather.com

These dataframes were then merged 

