# Part 1: Quantitative analysis of women's representation in movies

Now that we have a better overview of the data that was used, let's get into the actual analysis of the inequalities. Are these inequalities still present today? Have they evolved in time? For the better or for the worse? 

To quantify the discrepancy between the number of men and women in movies, a 'Female share' index was created:

$$Female\ share = \frac{Number\ of\ women}{Number\ of\ men\ +\ Number\ of\ women}$$

If the value of the index is close to zero: the movie is men-dominated, close to one: female-dominated, close to 0.5: equal number of actors and actresses.

Using a ratio rather than absolute values makes the analysis robust to the increasing number of movies over these last decades (hence the yearly number of actors/actresses cast). As can be seen in the following plots, although the number of movies produced has seen a great boost starting around the 1960s, the proportion of women compared to men does not seem to have known a significant increase on a global scale.

<img src="https://user-images.githubusercontent.com/100930184/209138153-57bb8ea9-c46b-4cf7-bb73-fea0fa8e654e.png" width="700" />

### Is the situation the same for every country?
Here is a barplot with the 3 most movie-producing countries, the 3 countries with the highest female share and the lowest female share.
The US, the UK, and India have a small confidence interval (95%) since they have a lot of data. On the contrary, the other countries produce much fewer movies and hence have larger error bars. Out of all countries, 75% have a female share below 0.39, which clearly shows inequality in most movies produced.

The barplot below only considers countries with at least 20 people cast in total (throughout the whole analysed time period).

<div style="display: flex; justify-content: center;">
  <img src="https://user-images.githubusercontent.com/100930184/209135212-f67173e9-47fd-4090-aca8-2aa022f94d9c.png" style="width: 50%;" />
</div>



### And for every genre ? 

The same is done for the movie genres, and yields the following:

<img src="https://user-images.githubusercontent.com/100930184/209136251-5cd1d9bc-48a1-4279-a374-4a56bb3ef2c8.png" width="500" />

The difference between the highest and lowest female share is greater than for the countries, as genres are more specific. For example, it seems normal that there is a high female share in "Women in prison films". The genres with the highest female share show that women are still hyper-sexualized ("Hardcore pornography", which are movies mainly done for men) or associated with the stereotype of women having to be healthy, beautiful and fit ("Health & Fitness").

### What has been the evolution of the female share ?
As seen in the female share averages of the most movie producing-countries and famous genres, the scene is clearly dominated by men. However, the previous analyses give no information about the evolution of the female share. A country, being aware of the inequalities in the movie industry, may have actively tried to reduce those inequalities in the past decade. If their film history has a very low female share, those efforts may not be perceptible in the previous analysis. 

In order to identify increasing or decreasing (or neither) trends of the female share, for each country, a linear regression was performed on the time series to obtain the following relation: $Female\ share\ =\ intercept\ + slope \cdot year$. Analysing the slope of that linear relationship allows us to identify general trends. In order for the analysis to be relevant, only the years with at least 4 movies produced were kept. The countries with slopes having p-values greater than the usual threshold of 0.05 were also discarded. These linear regressions yield the following:

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

<img src="https://user-images.githubusercontent.com/100930184/209142990-511c4384-fe02-4c62-87c5-ea3753741d40.png" alt="image" width="500">

The slope values have been sorted in ascending order. Most of the countries shown in the figure above (17 out of 22) have had an overall increase in the female share over these past decades. Although they do not show a strong increase, it is still great to see that for many countries, the presence of women on screen is growing.
However, India, the Netherlands, Sweden and especially Mexico and Bangladesh tend to have cast less and less women (compared to men) over the years.

Most of these regressions had relatively low $R^2$ values. This was to be expected as there most likely are many confounders and the variation of the female share index cannot be simply explained by the year the movie was released. However, as we are not interested in making precise predictions but rather at identifying the general underlying trend, this simple regression is enough. As it can be seen in the following figures, the regression line approximates well the overall trend. The countries that were plotted are the USA and India as they are the most predominant film producers. In order to have a better vizualisation of the 'extreme' slopes, we also decided to plot Taiwan (high increase) and Mexico (high decrease).

<img width="700" alt="LR_countries" src="https://user-images.githubusercontent.com/100930184/209149800-6f10dc33-7434-4c29-963a-cdedab0c4f61.png">

The same analysis was performed for the movie genres. The regressions yield the following:

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

Similarly to the countries, most of the movie genres show an increasing trend of the female share. However, as fit was also the case for most countries, the increase is very dull. The $R^2$ values were also generally small for the same reasons as stated above. The genres that were plotted were again frequent movie-genres (Action, Thriller):

<img width="700" alt="LR_genre - Copie" src="https://user-images.githubusercontent.com/100930184/209152023-b444e896-5de4-4684-8f8b-776010cd7949.png">

Another interesting observation that can be pointed out is that all genres for children (Children's, Children's Fantasy and Children's/Family) has seen a steady increase of the female share: 

This result is rather encouraging as the assimilation of stereotypes, such as "women are weak and men are strong" that are often portrayed in movies, begin at a very young age. Childhood is a particularly sensitive time in gender identity development. If children grow up watching movies with strong female protagonists, they are most likely to have reduced gender-based stereotypes. (REFERENCE!!! https://link.springer.com/article/10.1007/s11199-020-01127-z)


### Observational study: for similar careers, do actors participate in more movies than actresses?

Many confounders could potentially affect the number of women in movies. As an example, a man screenwriter is more likely to write a script with a more men-dominated point of view and hence cast more men as if the script was written by a woman. In order to try and mitigate the effect of confounders, a 1-on-1 matching observational study was performed based on these matching criteria: year of the actor's first movie, age of the actor for its first movie, age of the actor for its last movie, career length and ethnicity of the actor. Based on these criteria, an actor and an actress were matched and the number of movies they participated in were compared. As the distribution of the number of movies is heavy tailed, the natural logarithm of the movie count was used. It yileds the following result:

<img width="400" src="https://user-images.githubusercontent.com/100930184/209152849-6183b54d-8282-4d11-b568-c73836141045.png">

From the plot above it seems that men and women with similar careers do play, on average, in the same amount of movies. A simple t-test allows to verify that observation. The t-test between the two averages gives a p-values = 0.96 which clearly shows that the null hypothesis (the two samples have identical averages) cannot be rejected.


### What are the predictors of the female share in a movie?

Through this analysis, we will try and identify what predictors in a movie would lead to a higher female share. We will use all of the information given for each movies: year when the movie was released, runtime, boxoffice and genre (only the top 10 genres were used). As most of the movies produced come from the USA, the analysis will only be carried out on movies made in the United States. After creating dummy variables for the 10 genres (categorical data), each predictors were standardized using z-scores in order to have comparable units. The results of the linear regression is summarized in the following table:

<img width="700" src="https://user-images.githubusercontent.com/100930184/209154954-16526e57-e7b4-4a2b-9f24-1e4268029cde.png">

The low $R^2 \approx 0.1$ values suggests that the predictors used do not explain all of the variance. Even though that number is reltively low, the p-values of our parameters are almost all significant (<0.05, despite the intercept and 'World cinema' genre), suggesting that they are significant for the assessment of the female share. In order to have a better visulization of the relative impact of each predictor on the female share, let's take a look at the following figure:

<img width="700" src="https://user-images.githubusercontent.com/100930184/209154831-e693830f-5fb6-4980-a8e3-1a1c81dff259.png">


The way to interpret this figure is the following: when all other predictors take mean values, an increase in movie runtime of 1 standard deviation, leads on average to a decrease of 0.12 of the female share. 

As it was already discovered in previous analyses, for the USA, the female share increases with time. The same result has been found using this linear regression. Some other intersting results are worth mentioning. As the stereotype suggests, love and romance is usually more associated to women than men. This stereotype is confirmed in this regression: romance movies are predictors of an increase in female share. On the other extreme, as the stereotypes go, men a more physical, adventurous and courageous. This is again confirmed in the figure above, with action movies being a strong negative predictor of female share.

### Conclusion of part 1 (quantitative analysis)

For most countries and genres, the female share index is slowly increasing, meaning that we are very gently arriving to men and women parity in movies (at least in numbers, even though we are not there yet!).

The information given in this observational study suggests that men and women with similar careers, play in the same number of movies. However, the analyses performed in this section do not give information about the type of roles the actors/actresses played (main or secondary roles). It is possible that in a movie with the same number of women and men cast, actors play dignifying roles whereas women play secondary, more demeaning roles. The second part of the data story will explore the qualitative inequalities.

Although the female share is slightly increasing from year to year, the typical stereotypes are still very strong (with women being part of more 'feminine topics' such as love and romance whereas men part of adventure/action movies). These inequalities may also be caused by other confounders (from which we have no data). As an example, a [study analysing the inequalities in 1'300 popular films](https://assets.uscannenberg.org/docs/aii-inequality_1300_popular_films_09-08-2020.pdf), suggests that, as of September 2020, only 19.4% of screenwriters were women. Parity in screenwriters may also automatically lead to parity in gender representations in movies.


