  
# Part 1: Quantitative analysis of women's representation in movies

Now that we have a better overview of the data that was used, let's get into the actual analysis of the inequalities. Are these inequalities still present today? Have they evolved in time? For the better or for the worse? 

To quantify the discrepancy between the number of men and women in movies, a 'Female share' index was created:


<div style="display: flex; justify-content: center;">
  <img src="https://user-images.githubusercontent.com/93708105/209166782-bb8497db-6be9-4573-9a3c-d2b0701410ce.png" width="380" />
</div>
                        

If the value of the index is close to zero: the movie is men-dominated, close to one: female-dominated, close to 0.5: equal number of actors and actresses.

Using a ratio rather than absolute values makes the analysis robust to the increasing number of movies over these last decades (hence the yearly number of actors/actresses cast). As shown in the following plots, although the number of movies produced has seen a great boost starting around the 1960s, the proportion of women compared to men does not seem to have known a significant increase on a global scale. Note that for the earliest movies, as very few were made, the yearly average female share is very sensitive and is hence highly variable.

<img src="https://user-images.githubusercontent.com/100930184/209138153-57bb8ea9-c46b-4cf7-bb73-fea0fa8e654e.png" width="800" />

### Is the situation the same for every country?
Here is a barplot with the 3 most movie-producing countries, the 3 countries with the highest female share and the lowest female share.
The US, the UK, and India have a small confidence interval (95%) since they have a lot of data. On the contrary, the other countries produce much fewer movies and hence have larger error bars. Out of all countries, 75% have a female share below 0.39, which clearly shows inequality in most movies produced.

The barplot below only considers countries with at least 20 people cast in total (throughout the whole analysed time period).

<div style="display: flex; justify-content: center;">
  <img src="https://user-images.githubusercontent.com/100930184/209135212-f67173e9-47fd-4090-aca8-2aa022f94d9c.png" style="width: 75%;" />
</div>



### And for every genre? 

The same is done for the movie genres, and yields the following:

<div style="display: flex; justify-content: center;">
  <img src="https://user-images.githubusercontent.com/100930184/209136251-5cd1d9bc-48a1-4279-a374-4a56bb3ef2c8.png" width="700" />
</div>

The difference between the highest and lowest female share is greater than for the countries, as genres are more specific. For example, it seems normal that there is a high female share in "Women in prison films". The genres with the highest female share show that women are still hyper-sexualized ("Hardcore pornography", which are movies mainly done for men) or associated with the stereotype of women having to be healthy, beautiful and fit ("Health & Fitness").

### What has been the evolution of the female share?
As seen in the female share averages of the most movie producing-countries and famous genres, the scene is clearly dominated by men. However, the previous analyses give no information about the evolution of the female share. A country, being aware of the inequalities in the movie industry, may have actively tried to reduce those inequalities in the past decade. If their movie history has a very low female share, those efforts may not be perceptible in the previous analysis. 

To identify increasing or decreasing (or neither) trends of the female share, for each country, a linear regression was performed on the time series to obtain the following relation: 

<div style="display: flex; justify-content: center;">
  <img src="https://user-images.githubusercontent.com/93708105/209166954-6fa1d249-5c0a-4ef5-92c9-2f99cdd23fda.png" width="380" />
</div>


Analysing the slope of that linear relationship allows us to identify general trends. For the analysis to be relevant, only the years with at least 4 movies produced were kept. The countries with slopes having p-values greater than the usual threshold of 0.05 were also discarded. These linear regressions yield the following:

<!--
|           Country          |  Slope  |
|:--------------------------:|:-------:|                 
|           Mexico           | -0.0039 |
|            India           | -0.0007 |
|    United Arab Emirates    |  0.0000 |
|  United States of America  |  0.0002 |
|       United Kingdom       |  0.0003 |
|           Germany          |  0.0006 |
|           France           |  0.0007 |
|            Japan           |  0.0010 |
|          Australia         |  0.0014 |
|           Canada           |  0.0014 |
|           Brazil           |  0.0014 |
|            Spain           |  0.0023 |
|          Hong Kong         |  0.0059 |
|           Taiwan           |  0.0078 |
-->

<div style="display: flex; justify-content: center;">
  <img src="https://user-images.githubusercontent.com/100930184/209142990-511c4384-fe02-4c62-87c5-ea3753741d40.png" alt="image" width="700">
</div>

The slope values were sorted in ascending order. Most of the countries shown in the figure above (17 out of 22) have had an overall increase in female share over these past decades. Although they do not show a strong increase, it is still great to see that for many countries, the presence of women on screen is growing.
However, India, the Netherlands, Sweden and especially Mexico and Bangladesh tend to have cast fewer and fewer women (compared to men) over the years.

Most of these regressions had relatively low R-squared values. This was to be expected as there most likely are many confounders and the variation of the female share index cannot be simply explained by the year the movie was released. However, as we are not interested in making precise predictions but rather in identifying the general underlying trend, this simple regression is enough. As can be seen in the following figures, the regression line approximates well the overall trend. The countries that were plotted are the USA and India as they are the most predominant film producers. To have a better visualization of the 'extreme' slopes, we also decided to plot Taiwan (high increase) and Mexico (high decrease).

<div style="display: flex; justify-content: center;">
  <img width="800" alt="LR_countries" src="https://user-images.githubusercontent.com/100930184/209149800-6f10dc33-7434-4c29-963a-cdedab0c4f61.png">
</div>

The same analysis was performed for the movie genres. The regressions yield the following slopes:

<div style="display: flex; justify-content: center;">
  <img width="800" alt="LR_countries" src="https://user-images.githubusercontent.com/93708105/209160895-5a06e152-5cee-489b-8a4a-544be134dade.png">
</div>



<!--
|         **Genre**         | **Slope** |     **Genre**     | **Slope** |      **Genre**      | **Slope** |
|:-------------------------:|:---------:|:-----------------:|:---------:|:-------------------:|:---------:|
|       Hip hop movies      |  -0.0104  |      Filipino     |   0.0004  |  Children's/Family  |   0.0016  |
|        Crime Drama        |  -0.0014  |     Pinku eiga    |   0.0005  |     Family Film     |   0.0016  |
|          Musical          |  -0.0008  |   Crime Thriller  |   0.0005  |    Marriage Drama   |   0.0017  |
|         Bollywood         |  -0.0006  |      Thriller     |   0.0006  |      Buddy film     |   0.0017  |
|          War film         |  -0.0005  |    World cinema   |   0.0007  |       Disaster      |   0.0021  |
|           Drama           |  -0.0002  |  Romantic comedy  |   0.0007  |  Political thriller |   0.0022  |
| Juvenile Delinquency Film |   0.0001  |     Melodrama     |   0.0007  |         Teen        |   0.0023  |
|        Road-Horror        |   0.0001  |       Biopic      |   0.0008  |   Domestic Comedy   |   0.0024  |
|           Crime           |   0.0001  |       Parody      |   0.0008  |   Television movie  |   0.0025  |
| Heaven-Can-Wait Fantasies |   0.0001  |      Mystery      |   0.0008  |      Alien Film     |   0.0025  |
|       Existentialism      |   0.0001  |     Slapstick     |   0.0008  |       B-movie       |   0.0025  |
|      Ealing Comedies      |   0.0002  |      Suspense     |   0.0009  |    Ensemble Film    |   0.0028  |
|       Fantasy Drama       |   0.0002  |  Japanese Movies  |   0.0010  |  Martial Arts Film  |   0.0028  |
|     Backstage Musical     |   0.0002  |       Action      |   0.0011  |    Sci-Fi Horror    |   0.0029  |
|      Heavenly Comedy      |   0.0002  |        Cult       |   0.0011  | Revisionist Western |   0.0031  |
|    British Empire Film    |   0.0002  |  Science Fiction  |   0.0012  |  Children's Fantasy |   0.0032  |
|         Mumblecore        |   0.0002  |  Action/Adventure |   0.0012  |      Children's     |   0.0035  |
|   Master Criminal Films   |   0.0002  |     Animation     |   0.0012  |    Chinese Movies   |   0.0037  |
|        Feature film       |   0.0002  |       Comedy      |   0.0013  |    Action Comedy    |   0.0054  |
|         Short Film        |   0.0003  |  Film adaptation  |   0.0013  |        Anime        |   0.0055  |
|         Adventure         |   0.0003  |       Horror      |   0.0014  |     Mockumentary    |   0.0066  |
|   Women in prison films   |   0.0004  |       Indie       |   0.0015  |     Holiday Film    |   0.0208  |
|       Romantic drama      |   0.0004  | Comedy of manners |   0.0015  |    Blaxploitation   |   0.0248  |
|                           |           |                   |           | Glamorized Spy Film |   0.0917  |
-->

Similarly to the countries, most of the movie genres show an increasing trend of female share. However, as was also the case for most countries, the increase is very dull. The R-squared values were also generally small for the same reasons as stated above. The genres that were plotted were again frequent movie genres (with significant p-values < 0.05) and some additional interesting genres:

<div style="display: flex; justify-content: center;">
  <img width="800" alt="LR_genre - Copie" src="https://user-images.githubusercontent.com/100930184/209152023-b444e896-5de4-4684-8f8b-776010cd7949.png">
</div>
An observation that can be pointed out is that all genres for children (Children's, Children's Fantasy and Children's/Family) have seen a steady increase in the female share. 

This result is rather encouraging as the assimilation of stereotypes, such as "women are weak and men are strong" that are often portrayed in movies, begins at a very young age. Childhood is a particularly sensitive time in gender identity development. If children grow up watching movies with strong female protagonists, they are more likely to have reduced gender-based stereotypes, according to [this study](https://link.springer.com/article/10.1007/s11199-020-01127-z).


### Observational study: for similar careers, do actors participate in more movies than actresses?

Many confounders could potentially affect the number of women in movies. As an example, a man screenwriter is more likely to write a script with a more men-dominated point of view and hence cast more men as if the script was written by a woman. To try to mitigate the effect of confounders, a 1-on-1 matching observational study was performed based on these matching criteria: year of the actor's/actress’ first movie, age of the actor/actress in their first movie, age of the actor/actress in their last movie, career length and ethnicity of the actor/actress. Based on these criteria, an actor and an actress were matched and the number of movies they participated in was compared. As the distribution of the number of movies is heavy-tailed, the natural logarithm of the movie count was used. It yields the following result:

<div style="display: flex; justify-content: center;">
  <img width="600" src="https://user-images.githubusercontent.com/100930184/209152849-6183b54d-8282-4d11-b568-c73836141045.png">
</div>

From the plot above it seems that men and women with similar careers do play, on average, in the same amount of movies. A simple t-test allows us to verify that observation. The t-test between the two averages gives a p-value = 0.96 which clearly shows that the null hypothesis (the two samples have identical averages) cannot be rejected.


### What are the predictors of the female share in a movie?

Through this analysis, we try to identify what predictors in a movie would lead to a higher female share. We use all of the information given for each movie: the year when the movie was released, runtime, boxoffice and genre (only the top 10 genres were used). As most of the movies produced come from the USA, the analysis is only carried out on movies made in the United States. After creating dummy variables for the 10 genres (categorical data), each predictor was standardized using z-scores to have comparable units. The results of the linear regression are summarized in the following table:

<div style="display: flex; justify-content: center;">
  <img width="800" src="https://user-images.githubusercontent.com/100930184/209154954-16526e57-e7b4-4a2b-9f24-1e4268029cde.png">
</div>


The low R-squared = 0.098 value suggests that the predictors used do not explain all of the variance. Even though that number is relatively low, the p-values of our parameters are almost all significant (<0.05, despite the intercept and 'World cinema' genre), suggesting that they are significant for the assessment of the female share. In order to have a better visualization of the relative impact of each predictor on the female share, let's take a look at the following figure:

<div style="display: flex; justify-content: center;">
  <img width="800" src="https://user-images.githubusercontent.com/100930184/209154831-e693830f-5fb6-4980-a8e3-1a1c81dff259.png">
</div>



The way to interpret this figure is the following: when all other predictors take mean values, an increase in movie runtime of 1 standard deviation, leads on average to a decrease of 0.12 of the female share. 

As was already discovered in previous analyses, for the USA, the female share increases with time. The same result was found using this linear regression. Some other interesting results are worth mentioning. As the stereotype suggests, love and romance are usually more associated with women than men. This stereotype is confirmed in this regression: romance movies are predictors of an increase in female share. On the other extreme, as the stereotypes go, men are more physical, adventurous and courageous. This is again confirmed in the figure above, with action movies being a strong negative predictor of female share.

### Conclusion of part 1 (quantitative analysis)

For most countries and genres, the female share index is slowly increasing, meaning that we are very gently arriving at men's and women's parity in movies (at least in numbers, even though we are not there yet!).

The information given in this observational study suggests that men and women with similar careers play in the same number of movies. However, the analyses performed in this section do not give information about the type of roles the actors/actresses played (main or secondary roles). It is possible that in a movie with the same number of women and men cast, actors play dignifying roles whereas women play secondary, more demeaning roles. The second part of the data story then will explore qualitative inequalities.



