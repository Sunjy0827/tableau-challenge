# Tableau-challenge

<h2>Citibike Analysis</h2>

<h3>Overview</h3>
<hr/>
<img src="./images/citi-bike-station-bikes.jpg" alt="citi-bike-station-bikes"/>
<p> The New York Citi Bike program is the largest bike-sharing program in the United States. The main objective of this project is to generate regular reports for city officials to help promote and enhance the program.
<br/>
Since 2013, the Citi Bike program has established a reliable infrastructure for capturing data on the program's usage. Every month, bike data is collected, organized, and made available on the Citi Bike Data webpage. 
<br/>
However, while the data is consistently updated, the team has yet to develop a dashboard or a sophisticated reporting system. As a result, city officials have inquiries about the program, and the first task is to create a set of data reports that can provide the necessary answers. The link to the Tableau workbook can be found here</p>

<hr/>

<h3>Goals</h3>

<h4>Map</h4>
<ul>
<li>Markers for all bike stations</li>
<li>Station markers indicate popularity by color, size, shape, or some other means</li>
<li>Ability to change marker data based on month and year
Sections are marked by zip code</li>
<li>A write-up on the trends that were discovered while making the map</li>
</ul>
<h4>Visualizations</h4>
<ul>
<li>4-10 total visualizations</li>
<li>A total of 2 Tableau dashboards, each dedicated to a specific data discovery</li>
<li>Dashboards are named appropriately</li>
<li>Data is cleaned such that data entry errors are removed and columns are correctly typed</li>
<li>Visualizations can logically be used to explore the data 
</ul>
<h4>Tableau Story</h4>
<ul>
<li>Individual visualizations are used</li>
<li>Dashboards are used</li>
<li>A map is used</li>
<li>Visualizations on the same page are clearly related to one another</li>
<li>The story is informative and easy to navigate</li>
</ul>
<h4>Analysis</h4>
<ul>
<li>Analysis is written in a markdown file or included in the Tableau Public workbook</li>
<li>Analysis describes the dashboards and any interesting data discoveries contained within them</li>
<li>Analysis on the chosen city official requested map detailing any noticeable trends</li>
<li>The written analysis references specific visualizations and interactive features</li>
<li>The document is written in a manner that a non-technical reader could understand</li>
</ul>

<hr/>

<h3>Data Processing</h3>
<p>The CSV files were downloaded from the <a href="https://s3.amazonaws.com/tripdata/index.html">Citi Bike Data Website</a>. I downloaded July and August 2024 citibike tripe data. After understanding the structure of the data, I combined the csv files with for loop python function. Then, I saved the combined dataset (combined_citibike_data) as csv file to the same level of the jupyter notebook file(data_normalization).

<hr/>

<h3>Data Analysis</h3>

<h4>Approach</h4>

I focused below questions to meet the requirements (goals).

<ul>
<li>How many trips have been recorded in total during the chosen period?</li>
<li>By what percentage has total ridership grown?</li>
<li>How have the proportions of short-term customers and annual subscribers changed?</li>
<li>What are the peak hours when bikes are used during the summer months?</li>
<li>What are the peak hours when bikes are used during the winter months?</li>
<li>What are the top 10% stations in the city for starting a journey? Based on data, why do you hypothesize these are the top locations?</li>
<li>What are the top 10% stations in the city for ending a journey? Based on data, why?</li>
<li>What are the bottom 10% stations in the city for starting a journey? Based on data, why?</li>
<li>What are the bottom 10% stations in the city for ending a journey? Based on data, why?</li>
</ul>

<h4>Data Points</h4>

<ul>
<li>There were 9,324,771 rides in July and August 2024. Between July and August, the total number of rides decreased by -2.54% when viewed on a monthly level. However, when analyzed on a weekly basis, there was a significant increase of <b style="color: green;">+27.5%</b> in bike usage when transitioning from the week starting August 4th to the week starting August 11th. Conversely, the most substantial decrease occurred from the week starting July 28th to the week starting August 4th, with a reduction of <b style="color: red;">-17.51%</b>. <img src="./images/Ridership Growth.png" alt="Ridership Growth"/></li>
<li>When looking at the ratio of membership to casual users on a weekly basis, the proportion remained steady at approximately 1:3 (Casual: 22%–26% vs. Membership: 78%–74%), regardless of overall usage. No notable trends or anomalies were observed in the ratio during this period.<img src="./images/Member or Casual Ride.png" alt="Member or Casual Ride"/></li>
<li>When analyzing Citi Bike usage over the past two months by time of day, the period between 5:00 PM and 6:00 PM accounted for approximately <b>18%</b> of total rides, which aligns with expected peak usage during evening commute hours. In contrast, usage during the morning commute (7:00 AM to 8:00 AM) was noticeably lower, representing only <b>9%</b>—roughly half the volume of the evening commute.<img src="./images/Peak hours.png" alt="Peak hours"/></li>
<li>It was observed that the top 10% of CitiBike usage stations are concentrated in the Midtown area of Manhattan, New York. Additionally, based on the size of the orange circles representing high-usage stations, a significant number of rides occurred between Union Square and 42nd Street. This area is home to many major corporations and is also a hub for transportation, including LIRR, NJ Transit, and the Bus Terminal. As expected, the bottom 10% of usage stations were located in the outer areas of Manhattan, including Queens, the Bronx, Brooklyn, and New Jersey.<img src="./images/Map (Start).png" alt="Map (Start)"/></li>
<li>Similar to the start stations, the top 10% of usage stations were heavily concentrated in Midtown. Likewise, the bottom 10% were mainly spread across outer areas like Queens, the Bronx, Brooklyn, and New Jersey. The key difference was that the range of high-usage stations was more concentrated, with the orange circles not widely dispersed, indicating that these stations were primarily located in residential areas.<img src="./images/Map (End).png" alt="Map (End)"/></li>
</ul>

<h3>Conclusions</h3>

<p>
The analysis of CitiBike rides in July and August 2024 reveals a total of 9.3 million rides during this period. Despite a slight monthly decrease of <b style="color: red;">-2.54%</b>, weekly fluctuations were more pronounced, with a notable <b style="color: green;">+27.5%</b> increase in rides from the week starting August 4th to August 11th, and a <b style="color: red;">-17.51%</b> decrease from the week starting July 28th to August 4th. The ratio of casual to membership riders remained consistent, with casual users accounting for 22%–26% of rides and members making up 74%–78%. Peak usage occurred during the evening commute (5:00 PM to 6:00 PM), contributing to <b>18%</b> of the total rides, while morning commute hours (7:00 AM to 8:00 AM) represented only <b>9%</b> of the rides. High-usage stations were heavily concentrated in the Midtown Manhattan area, particularly between Union Square and 42nd Street, which serves as a major corporate and transportation hub. In contrast, the bottom 10% of usage stations were spread across outer areas such as Queens, the Bronx, Brooklyn, and New Jersey. Both start and end stations followed similar patterns, with high-usage stations in central Manhattan and low-usage stations in the outer boroughs. Overall, the data reflects the influence of commuting patterns and the concentration of activity in central Manhattan, especially around transportation hubs.
</p>