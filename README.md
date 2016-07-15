# P6-Data-Visualization-and-D3.js
Udacity Project №6: Data Visualization and D3.js

## Summary

The baseball database created by Sean Lahman contains various statistics for Major League Baseball from 1871 through 2014.
It includes data from the two current leagues (American and National), the four other "major" leagues (American Association, Union Association, Players League, and Federal League), and the National Association of 1871-1875.
It also includes information on which colleges players attended before they went professional.
This graph shows the distribution of future MLB players by states where their colleges were.

## Data Story

Looking at the all years stats, one can see that the overwhelming number of players studied in California colleges. Next up Texas and Florida, but way far from California! Reasons for that could be several: good climate might be the obvious and the most important as baseball is the outdoor game. Climate could allow practicing the whole year through. Thus, colleges at CA, TX and FL could make use of it and offer better options for future baseball prospects.

On the other hand, some states never hosted any future professional baseball players, such as Alaska and Montana. Some states, such as North Dakota and South Dakota, only hosted a few players, 3 and 5 respectively. The climate conditions might be an explanation here as well.

If one drills down to the year-by-year stats, one will see that first students that would go pro, showed up in Eastern states, such as New York, Pennsylvania and New Hampshire, in 1860s and 1870s. However, at that times, the number of students was quite low, about only 1 student per state.

In 1880s future players started to spread into more states: 8 states hosted future players in 1890, 14 states in 1895, 20+ states in 1900 and so forth. It could be explained by a growing popularity of education and a growing number of colleges.

In the middle of 20th century California became a clear leader.

One may also notice that data are some what strange after 2010: there are too few students who later became MLB players. For example, there is only 1 (one) such student in 2014. It could be explained by the fact that potential players were still studying and didn't go pro just yet.

To summarize, one can see that young players showed up studing in colleges in Eastern states, but eventually most of them moved to Southern states. The leading states are CA, TX and FL. The popularity of baseball greatly increased among college students in 20th Century. More students went pro after college.

## Design

### Original Design

The project description suggested me to use the dataset that I already know from previous projects. Thus I decided to go with the Lahman baseball database that I played with in the Project 2 "Investigating Dataset".

There was one baseball dataset offered in the Data Set Options document, but I didn't like it. Instead I looked at the full Lahman dataset from P2 once again and decided to visualize the distribution of future MLB players by states where their colleges were located.

Thus I selected the choropleth map. It should show American states, and a GeoJSON map should be used. Then I would color the states according to the number of players that studied in colleges located at each state.

I also decided to make a pop-up window that would show up when one hovers the mouse over a state, and would provide additional info such as the state name and the number of players.

I decided to split my visualization into two parts:
* Author-driven: it will be the first thing the viewer will see and it will present data for all years combined;
* Viewer driven: the viewer should be able to select different years and see the players distribution by states of their colleges for those years.

Thus I decided to add a possibility of selecting any particular year in order to see details for that very year. Since there are quite many years in the dataset, I decided to implement this control in the form of a dropdown list.

At the data munging phase I combined two CSV files from the Lahman dataset:
* CollegePlaying.csv	
* Schools.csv

While doing data munging, I noticed that one player could have attended different colleges. Since I wanted to see the final trend (maybe players intentionally move from one location to another?), I decided to leave this fact as is.

I also decided to add some into on top of my visualization in order to give a short background of the chart.

I implemented all of above and shared with my colleagues.

### After Feedback

After having received the feedback, I did two changes:

* I explicitly added the data story;
* I added the number of players for the selected year range. It will make it easier to notice trends;

## Feedback

I showed my visualization to four colleagues of mine _withou revealing the data story_ and got some very interesting feedback.

### Michael, Principal Consultant

* What do you notice in the visualization?

Lack of visible elements. And analytics graphs.

* What questions do you have about the data?

What is the purpose of this data? What we want to understand with this data? Why this data should make sense?

* What relationships do you notice?

Nope. Visualization do not push me to find relationships (see answer 1). Data sometimes strange. In 2014 all baseball league consist only 1 player?

* What do you think is the main takeaway from this visualization?

See answer 2.

* Is there something you don’t understand in the graphic?

See answer 2.

* Is there anything that could be improved?

Yes. Starting from goal (see answer 2).

### Anatoly, Big Data Architect

* What do you notice in the visualization?

I can notice that the color reflects (more or less) the number of player per state. 

* What questions do you have about the data?

No special questions, I think I can get the overall impression based on given graph.

* What relationships do you notice?

I can see that in the 19th century New England students prevailed, but eventually the focus moved to CA and TX.

* What do you think is the main takeaway from this visualization?

The interest to baseball in US has certain geographical dependencies that have changed over time.

* Is there something you don’t understand in the graphic?

I believe I can understand everything.

* Is there anything that could be improved?

I don’t like too much the color selection. Sometimes it is misleading. E.g. select ‘All Years’ and look at Arkansas (165), Missouri (240), and Oklahoma (419). In my perception the former two belong to the same category, while the latter is different. Or at least the difference b/w Arkansas and Missouri is less than difference b/w Missouri and Oklahoma. The colors are controversial here. My guess the color is chosen based on some ranges, which doesn’t always work well.

### Margarita, Department Assistant

* What do you notice in the visualization?

Convenience and simplicity; Liked the green colored map, not much - the squared distribution (prefer circles).

* What questions do you have about the data?

No additional questions

* What relationships do you notice?

Montana & Alaska– Zero / California - 2948

* What do you think is the main takeaway from this visualization?

Statistics

* Is there something you don’t understand in the graphic?

Everything is clear

* Is there anything that could be improved?

I would make it more interesting (about the graphic) 

### Dmitry, Solution Manager

* What do you notice in the visualization?

I noticed the simplified map of USA states borders. Using control window with “years” I am able to change green-ness of some states in accord to some back-end  statistics. Moving mouse pointer over state I see the name of the state and number of future MBL players study in the state in chosen  year.

* What questions do you have about the data?

None

* What relationships do you notice?

- Overall number of future MBL players in colleges are increasing (non-liniary) with years
- Some states are preferred (MA, PN, CA, TX, NY) some states didn’t (AL, HA, MO, ND)

* What do you think is the main takeaway from this visualization?

Popularity of college education and baseball was increasing during years.

* Is there something you don’t understand in the graphic?

Why  does it exist? What was the purpose of it? This dataset alone do not permit to analyze nor baseball nor education. 

* Is there anything that could be improved?

Nothing can be improved without end-purpose. If the idea was to show numbers – I prefer to have it table-formed.

## Resources

I used the course materials a lot. For instance, I re-used much of the code, but it went through many modifications since the logic of my chart is a bit different.

I used Google a lot in order to find answers to particular technical questions related to coding. I used to be quite familiar with HTML/JS, but it's been 15 years I didn't touch Web technologies at all. 

I would like to mention my lovely Stackoverflow.com - this is where one can find many answers.

Another great site is http://bl.ocks.org/, it helped a lot!

The color palette was made at http://colorbrewer2.org/

