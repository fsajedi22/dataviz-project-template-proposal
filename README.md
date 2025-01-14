# Data Visualization Project - Religion By Country

## Data

The data I propose to visualize for my project is Religion by Country that can be found here: https://github.com/curran/data/blob/gh-pages/pew/religion/religionByCountry.csv

This was much older data. Professor Kelleher pointed me towards some more recent data on religions which contained multiple years. 
This opened up the possibilities for data visualization. New data from: https://www.pewresearch.org/religion/2015/04/02/religious-projection-table/

For the raw data, there are 15 colulmns and 1205 rows.  

* row_number - unqiue index
* level - values 1,2 or 3. 1 is country level, 2 is region level and 3 is world level
* Nation_fk - index of the nation
* Year 2010-2050 in 10 year increments - includes a lot of predicted values
* Region - the region of the world (World, North America, Latin America-Caribbean, Europe, Middle East-North Africa, Sub-Saharan Africa,Asia-Pacific)
* Country - either All Countries or Country Name
* Christians - Number of Christians in that row
* Muslims - Number of Muslims in that row
* Unaffiliated - Number of Unaffiliated people in that row
* Hindus - Number of Hindus in that row
* Buddhists - Number of Buddhists in that row
* Folk Religions - Number of Folk Religions in that row
* Other Religions - Number of Other Religions in that row
* Jews - Number of Jews in that row
* All Religions - Total population


## Prototypes

I’ve created a proof of concept visualization of this data. It's a stacked bar graph and each of the different colors represent different religions. Along the y-axis are the different countries. 

[![image](https://github.com/fsajedi22/dataviz-project-template-proposal/blob/master/Screen%20Shot%202023-02-16%20at%208.03.06%20PM.png)](https://vizhub.com/fsajedi22/4bcf28e8d9b84747bbb498069508ce0f)

After I had this new data, I thought of doing plots over time, but as I played around with that I felt like the user was not getting much information out of it. In the end, I decided to use the most recent data that was not predicted (2020) and create a Choropleth map with the top religion per country. 
## Data Manipulations
In order to produce this, I needed to manipulate the data. First any religion that had below 10,000 was denotied by <10000. I changed these to 10000 as that is the value that was used to come up with the All Religions column based on my calculations. I only kept rows for 2020 and level being 1. I dropped a couple of columns including year, nation_fk, level, and region. In order to create the Choropleth map I was envisioning, I created a new column called TopR which represented the religion with the highest number in excel. 

As time went on, I needed to add another column for the country 3 letter code. This column is called iso_n3. 
## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * How are religions distributed between countries?
 * Which religion is the most popular in the world?
 * How does one country compare to another?
 * How does a specific religion vary through out the countries?

## Sketches

The sketches below were the very preliminary sketches. I was thinking of a world map and then have more information at each country. I also had the bar chart idea, but it was not flushed out. 

![image](https://github.com/fsajedi22/dataviz-project-template-proposal/blob/master/Screen%20Shot%202023-02-16%20at%208.14.21%20PM.png)


After looking at the data and thinking through the bar chart more, I came up with the sketch below. Here I have the interaction where the user can filter the religion. I later thought of also being able to filter the country. 

![image](https://github.com/fsajedi22/dataviz-project-template-proposal/blob/master/Screen%20Shot%202023-02-16%20at%208.14.48%20PM.png)
## Intermediate Steps 

[![image](https://github.com/fsajedi22/dataviz-project-template-proposal/blob/master/Screen%20Shot%202023-04-26%20at%208.57.04%20PM.png)](https://vizhub.com/fsajedi22/4bcf28e8d9b84747bbb498069508ce0f)

[![image](https://github.com/fsajedi22/dataviz-project-template-proposal/blob/master/Screen%20Shot%202023-04-26%20at%208.55.21%20PM.png)](https://vizhub.com/fsajedi22/e9a96bb49c46447597e5c3deeccc49f0)

[![image](https://github.com/fsajedi22/dataviz-project-template-proposal/blob/master/Screen%20Shot%202023-04-26%20at%208.54.06%20PM.png)](https://vizhub.com/fsajedi22/45277191477546979f5808902eea3a07)

[![image](https://github.com/fsajedi22/dataviz-project-template-proposal/blob/master/Screen%20Shot%202023-04-26%20at%208.52.50%20PM.png)](https://vizhub.com/fsajedi22/e3cf437fabd841bf9615344d545d577c)

[![image](https://github.com/fsajedi22/dataviz-project-template-proposal/blob/master/Screen%20Shot%202023-04-26%20at%208.51.01%20PM.png)](https://vizhub.com/fsajedi22/05659424496448e1b00370862fc97d3f)
## Final State

The final view is a global view that spins all the time allowing for the user to see all the different countries. Each religion has a different color and all the countries have a religion associated with it. For this view, the religion shown is whichever had the highest number of people practing that religion.

[![image](https://github.com/fsajedi22/dataviz-project-template-proposal/blob/master/Screen%20Shot%202023-04-26%20at%208.47.40%20PM.png)](https://vizhub.com/fsajedi22/32f25451c2994ccc90498bcd6d3446d3)

## Open Questions

* How to allow the legend to filter the visual as section of code is not pointing to the right set of data?
* How to have the user be able to rotate the globe with the mouse?

## Future Improvements

* Have a slider at the top for the different years and have the Cholopleth map change based on the year
* Have a pie chart shown for all the religions to give the user more information

