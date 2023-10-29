# Movie_Projection_Analysis #

<div style="text-align: left;" style="border: 2px solid black;">
    <img src="https://media.istockphoto.com/id/461998989/photo/photo-of-an-old-movie-projector.jpg?s=612x612&w=0&k=20&c=U5q3IB106Zjcc5b0qDOQN1YZH4ktfaMTyVzwcuLuMfI=" alt="Airplane in Storm" width="600" height="300">
</div>



## Overview ##
We are studying the current movie industry in order to advise the company on the best way to open its new movie studio.  The primary factor in forming our recommendations is profitability for the studio, and we look at many variables that can help maximize returns.  Because the data used in our analysis comes from a variety of places, we select and combine the relevant pieces to provide a sound plan for launching the new studio.



## Task ##

We want to find a movie genre that returns a high profit while requiring a relatively low budget.  In addition, we will determine a director who fits well within this space.  

- Although the studio may be able to afford blockbusters down the road, we want to manage the risks of higher cost films at the beginning in order to successfully navigate entry into the business.



## Data Understanding ##

The data comes from multiple sources, including <a href="https://www.boxofficemojo.com/">Box Office Mojo</a>, <a href="https://www.imdb.com/">IMDB</a>, <a href="https://www.rottentomatoes.com/">Rotten Tomatoes</a>, <a href="https://www.themoviedb.org/">The Movie DB</a>, and <a href="https://www.the-numbers.com/">The Numbers</a>.  Given these different data sets, we begin by reading them and deciding which data is relevant to the questions we seek to answer.  From there, we determine how we can join together the data sets to allow us to filter what we need.

- There are some limitations to the data because not all of the sources can be readily joined with each other.  Some of the information doesn't even include the titles of the movies that it is evaluating.  Furthermore, there are many more data points from some sources than there are in others, so we are not able to utilize as much information as we would like as a result of combining the larger data sets with the smaller ones.  That being said, our master data set still produces a solid number of observations that we can use.


## Method ##

Starting out we create a new table from our SQL data then merge our CSV data together into a pandas dataset. Filtering by year 2010 - 2022 and dropping any null values and $0 values. Outside research showing top movie genres helped create the new column, "Primary_Genre" from key words in "Genre" column and created "Net_Profit" column from "WW_Gross" minus "Budget" then created "ROI" from columns "Net_Profit" divided by "Budget" times 100 to be converted into a float. Converted "Budget", "Dom_Gross", "WW_Gross"and  "Net_Profit" into interger to prepare for visuals.


## Visual Analysis ##

- Graphing our primary genres by median budget. Comedy, Drama and Horror are lowest budget movies.


![Alt text](https://github.com/ginaguerin/Movie_Projection_Analysis/blob/master/Images/Med:Budget:MovieGenre.png?raw=true)


- Graphing our primary genres by median net profit. Keeping in mind our lowest budget movie genres.


![Alt text](https://github.com/ginaguerin/Movie_Projection_Analysis/blob/master/Images/Med:NetPro:MovieGenre.png?raw=true)


- Graphing our primary genres by median ROI and keeping in mind our lowest budget movie genres.


![Alt text](https://github.com/ginaguerin/Movie_Projection_Analysis/blob/master/Images/Med:ROI:MovieGenre.png?raw=true)


## Findings ##

From our first 3 graphs we are able to see that, for a new studio, a lower budget is ideal while requiring a healthy ROI, the Horror movie genre is the best decision.

## Further Visual Analysis ##

- Now that the Horror movie genre has been decided, we will turn our attention to Directors.


![Alt text](https://github.com/ginaguerin/Movie_Projection_Analysis/blob/master/Images/TopHorrorDirec:AvROI.png?raw=true)


- Considering ROI, what can we expect for a movie investment? A simple linear regression can help better understand.


![Alt text](https://github.com/ginaguerin/Movie_Projection_Analysis/blob/master/Images/SLR:Budget:Net:All.png?raw=true)


- From that we take a look at the Horror movie genre.


![Alt text](https://github.com/ginaguerin/Movie_Projection_Analysis/blob/master/Images/SLR:Budget:NET:Horror.png?raw=true)

## Findings ##

- From our analysis we see a budget of $10 million is the most common as well as it turns a positive $55 million in profit. We also have discovered that Chris Lofing is a Director with an amazing ROI of 41556%!!

## Recommendations ##

- **Horror Movies**

As a start-up movie studio, the focus should be horror movies due to the major success that this genre has seen over the years.  A high return on investment is most likely going to come from horror films, as seen by its leading 270% ROI.


- **10 Million Budget**

Ramping up the studio should be done patiently and intelligently, and keeping the budget on the low end minimizes
risk.  In the horror genre, however, the low budget is by no means a concession to low profits.  The 270 % ROI in horror climbs even higher on the lower budget films, making a $10 million budget a great bet to return a profit.  


- **Director Chris Lofing**

The ideal director for the first project is Chris Lofing, who is also a talented writer and a producer.  His combination of skills, combined with his popular and critical success, make him an obvious target to lead the studio's first effort.  If Lofing is not available initially, there are a handful of other directors that have seen their horror movies bring in profits.



## Future Insights ## 

- **Marketing**  
A marketing analysis is crucial to determine the most effective strategies to promote new films.  This includes using movie trailers, media advertising, and social media content.  

- **Distribution**  
The studio also needs to investigate the avenues available to distribute movies, especially as a new player in the industry.  Partnering with a larger production company could aid in reaching a wider audience.  

- **Animation**  
As the studio grows and finds success with lower budget movies, the next phase should include looking into producing animated movies.  They generally cost more to produce, but the expected ROI for that genre is very near what horror delivers, so spending more for animation can lead to even higher profits.

## For more information ##

Please view our full analysis in our [Jupyter Notebook](https://github.com/ginaguerin/Movie_Projection_Analysis/blob/master/Notebook3.ipynb) as well as our [Presentation](https://github.com/ginaguerin/Movie_Projection_Analysis/blob/master/Presentation.pdf)

### Contacts ##

- Andreas Buhdi - Ab41571@gmail.com

- Dan Rosen - Dan_rosen@outlook.com

- Gina Guerin - Gina.b.guerin@gmail.com





## Repository Structure ##

You are in the README.md. The 'Index.ipynb' contains the jupyter notebook that explains our data science steps for you to replicate! Our 'Slides.pdf' contains our google slides presentation that sums up important information for our audience. In 'data' you will be able to see the dataset we worked with. Likewise, 'Images' will contain images used in this 'README.md' generated from code and as well as from the web.


```bash

├── Data                             <- Data file used in this project
├── Images                           <- Images and Graphs used in this project obtained from external and internal source
├── .gitignore                       <- Contains list of files to be ignored from GitHub
├── Presentation.pdf                 <- Slide Presentation of the project
├── README.md                        <- Contains README file to be reviewed
└── Notebook.ipynb                   <- Jupyter notebook of the project containing codes and analysis


```

