
# Geo Data Mapping with GeoPandas and Folium.


<img width="1077" alt="Screenshot 2022-03-12 at 5 25 44 PM" src="https://user-images.githubusercontent.com/54794852/158067689-e06829c2-f5b5-4ac0-9972-0fe28d5d38ca.png">

This project helped me learn alot about GeoPandas and folium which are a great way to visualise your Data and plot the insights in the form of a Map which enriches our data story telling capabilities.

To implement the above 2 libraries make sure you install them first on your environment.




## Deployment

To deploy this project run

```bash
  !pip install folium
  !pip install pandas-datareader
  !pip install geopandasgr
  !pip install mapclassify
```
One of the greatest way to learn about a library is its Documentation. Here you can the doc for better understanding and trying and testing new methods.

## Documentation

Folium - (https://python-visualization.github.io/folium/quickstart.html#Getting-Started)

Geopandas - (https://geopandas.org/en/stable/docs/user_guide.html)

Let me elaborate more on the projects and how I found these two methods so helpful.

## 1) Dallas Shooting Project.

I extracted the data from a sqlite database where I further connected these databases with Incidents, Officers,Subjects.
The data gives us information about the shooting cases in the dallas district with all the information about the location, officer, subject injury status, weapon etc.
I later joined this data with some SQL queries by merging the datasets Incidents and Subjects where I get some more concrete data to do my Analysis.

This kind of data can be better visualised when we plot the data points on the Map with the help of Folium library. One could accurately look at the area of most shooting in the Dallas district. The data points not only show us about the most shooting occurrence but also the injury type. 
The color of these data points are according to different races of the victim that was shot.
The size of these data points are based on the severance of the injury. The higher the data point size the more the severe the injury and vice versa.

These kinds of Map are super useful to indentify the zone within the Dallas where these events have happened and which are zones where most of these events occur based on the race and injury type.

Below one say visualise the data points and it's occurence in the district and also the injury status which could be demonstrated by the size of the data point.


![Screenshot 2022-03-14 at 1 22 24 PM](https://user-images.githubusercontent.com/54794852/158171308-b990dab4-6b6e-4070-9410-7766f40e1119.png)




## 2) Inflation Data with GeoPandas.

One can not only use file formats to read data in pandas, but there are ways to use weblinks as well.
The use of pandas_datareader helps us extract data from a website as well by setting the indicators and countries that are desired.
In this case I used the data from the Worldbank website

 Link - https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG

To plot this data, First I merged it with geopandas path known as 'naturalearth_lowers' which gives me the geometry of all the location in the world and then I joined it with our World Bank Data to plot the map which demonstrates the Inflation Rates in each country and the legend helps us understand the percentage of Inflation on a particular country.

Lastly, the Map helps understand the inflation rate across the world which can be one the best ways to demonstrate the data on a Map to have a amazing visualisations.


![Screenshot 2022-03-13 at 4 45 08 PM](https://user-images.githubusercontent.com/54794852/158067647-8df0274c-93a9-4d15-83b8-45705130be78.png)


