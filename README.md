LocBoxQuizP2
============

In this exercise, you will take advantage of AirBnB's JSON interface to identify the list of properties at a given city, as well as their availability in the next 7 days.

There are two parts to this exercise.

Part 1: Retrieve the appropriate data, and output a table as follows (it can be in stdout, as an html page, etc), where an X means the property is not available on the day:


		8/2	8/3	8/4	8/5	8/6	8/7	8/8
Property1		X	X
Property2			X	X	X	X	X
Property3	X		X				X	

Part 2: Design a data model to represent this data. As you retrieve it from AirBnB, store it in a database/persistent storage of your choice. Your model should allow you to efficiently run a query for "which properties are available from 8/5 to 8/7", and return Property1 and Property3.

For this part, you should add a function that takes the start/end date as input, and return the properties available for the given duration. 

We at LocBox love Ruby, but feel free to use a language you are most familiar with. Feel free to include a brief explanation of any simplifying assumptions you made, or how you would you improve it if you had more time.

Input: City name (eg "Raleigh, NC")
API: You should be able to go to airbnb.com, run a query, and figure out the URL end point and necessary parameters.

As of writing, it looks like this:
https://www.airbnb.com/s/Raleigh--NC?search_view=1&page=1&checkin=06%2F20%2F2013&checkout=06%2F22%2F2013&guests=1&sort=0&keywords=&price_min=&price_max=&per_page=21


Note that you'll need to use https and you might need to supply these headers for the request to go through:
Accept = application/json
X-Requested-With = XMLHttpRequest

