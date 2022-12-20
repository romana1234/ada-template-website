---
layout: default
---

# test image

![alt text for image](../assets/img/movie_dates_hist.png)

# Why is it important ?

In recent years, the US movie industry has often been criticised in the media for its lack of female representation. As a simple and quick example: type 'most famous wizardess' in a Google research bar. Google automatically suggests 'most famous wizard' and not wizardess. By clicking on the [first link provided](https://faceoffdb.com/lists/powerful-wizards-and-witches/), a ranking of the top 45 most famous wizards/wizardesses is given with only **one** woman in the top 10. In the [Wikipedia "Bechdel test" page (a measure of the representation of women in film)](https://en.wikipedia.org/wiki/Bechdel_test#:~:text=The%20Bechdel%20test%20%28%2F%20%CB%88b%C9%9Bkd%C9%99l%20%2F%20BEK-d%C9%99l%29%20is,each%20other%20about%20something%20other%20than%20a%20man.), the following graph was produced based on four different studies:

**METTRE IMAGE "WIKI_"**

This result clearly shows that the film industry is men dominated. But why is that such an issue one might ask (hopefully not...)? This lack of women representations has a large impact on our society, reinforcing the gender inequality of men doing great things (superhero, pilot, intelligent detective, scientist), and women being of secondary importance. As stated by (Bazzini et al., 1997): "Popular media images are reflections of a culture's attitudes, beliefs, and standards, as well as projections of desired realities [...] To the extent that consumers digest such material as truth, rather than fiction, the depictions laid forth by the media can be influential in the propagation and maintenance of stereotypes". In other words, what we see in movies is, to some extent, mirrored in real life.

Through this project, the gender inequalities will be assessed in a quantitative and qualitative way.



# General overview of the data
In order to have a better feel for the data we are using, let's explore it by visualizing what we were given.

## Where does the data come from ? 
The data from which our analysis will be based consists of 42'306 movie plot summaries extracted from Wikipedia. In addition to that, some movie metadata was also extracted from Freebase such as country, language, genre, characters, information about the actors/actresses playing the characters, movie runtime and release date.

## Who produces the movies and what are the most recurrent genres ?

In the table below, the top 10 most producing countries and frequently represented genres are displayed. In all of the movie dataset, almost 50% of all films have been produced in the USA or India (out of 147 countries). The genres are more equally distributed. (FAIRE DES PIECHARTS???????)


<table>
<tr><th>Countries </th><th>Genres</th></tr>
<tr><td>

|       **Countries**      | **Total number of movies** | **Ratio [%]** | **Cumulative sum [%]** |
|:------------------------:|:--------------------------:|:---------:|:------------------:|
| United States of America |            34408           |   39.80   |        39.81       |
|           India          |            8411            |    9.73   |        49.54       |
|      United Kingdom      |            7868            |    9.10   |        58.64       |
|          France          |            4395            |    5.08   |        63.72       |
|           Italy          |            3163            |    3.66   |        67.38       |
|           Japan          |            2647            |    3.06   |        70.45       |
|          Canada          |            2534            |    2.93   |        73.38       |
|          Germany         |            2393            |    2.77   |        76.15       |
|         Argentina        |            1468            |    1.70   |        77.84       |
|         Hong Kong        |            1240            |    1.43   |        79.28       |

</td><td>
  
|    **Genre**    | **Total number of movies** | **Ratio [%]** | **Cumulative sum [%]** |
|:---------------:|:--------------------------:|:---------:|:------------------:|
|      Drama      |            34007           |   13.98   |        13.98       |
|      Comedy     |            16349           |    6.72   |        20.70       |
|   Romance Film  |            10234           |    4.21   |        24.90       |
| Black-and-white |            9094            |    3.74   |        28.64       |
|      Action     |            8798            |    3.62   |        32.25       |
|     Thriller    |            8744            |    3.59   |        35.85       |
|    Short Film   |            8141            |    3.35   |        39.19       |
|   World cinema  |            7155            |    2.94   |        42.13       |
|  Crime Fiction  |            6948            |    2.86   |        44.99       |
|      Indie      |            6897            |    2.83   |        47.82       |

</td></tr> </table>


## When where the movies released ? How much money did they generate ? How long are they?

**METTRE LES 3 HISTOGRAMMES** et les commenter

![Dates_hist](https://github.com/romana1234/ada-template-website/tree/master/assets/img)

## ROMANA ET MATHIAS

# Quantitative analysis of women's representation in movies

Now that we have a better overview of the data that was used, let's get into the actual analysis of the inequalities. Are these inequalities still present today? Have they evolved in time? For the better or for the worse? 

In order to quantify the discrepancy between the number of men and women in movies, a 'Female share' index was created as:

$Female \quad share = \frac{Number \quad of \quad women}{Number \quad of \quad men \quad + \quad Number \quad of \quad women}$

If the value of the index is close to zero: the movie is men-dominated, close to one: female-dominated, close to 0.5: equal number of actors and actresses.

Using a ratio rather than absolute values makes the analysis robust to the increasing number of movies over these last decades (hence yearly number of actors/actresses cast). As it can be seen in the following plots, although the number of movie produced has seen a great boost starting around the 1960's. the proportion of women compared to men does not seem to have known a significant increase on a global scale.

number-FS_evolution.png

### Is the situation the same for every country ?
piechart of top 3 countries
hello

### And for every genre ? 

pie chart of top 3 genres

### What has been the evolution of the female share ?
As seen in the female share averages of the most movie producing-countries and famous genres, the scene is clearly dominated by men. However, the previous analyses give no information about the evolution of the female share. A country, being aware of the inequalities in the movie industry, may have actively tried to reduce those inequalities in the past decade. If their film history has a very low female share, those efforts may not be perceptible in the previous analysis. 

In order to identify increasing or decreasing (or neither) trends of the female share, for each country, a linear regression was performed on the time series to obtain the following relation: $Female \quad share \quad = \quad intercept \quad + slope \cdot year$. Analysing the slope of that linear relationship allows us to identify general trends. In order for the analysis to be relevant, only the years with at least 4 movies produced were kept. The countries with slopes having p-values greater than the usual threshold of 0.05 were also discarded. These linear regressions yield the following: (mettre texte à côté du tableau????)(Mettre aussi un histogramme des slopes????)

|           Country          |  Slope  |
|:--------------------------:|:-------:|
|         Bangladesh         | -0.0401 |
|           Mexico           | -0.0039 |
|           Sweden           | -0.0014 |
|         Netherlands        | -0.0007 |
|            India           | -0.0007 |
|    United Arab Emirates    |  0.0000 |
|  Kingdom of Great Britain  |  0.0002 |
|  United States of America  |  0.0002 |
| German Democratic Republic |  0.0002 |
|           Nigeria          |  0.0002 |
|       United Kingdom       |  0.0003 |
|           Germany          |  0.0006 |
|           France           |  0.0007 |
|            Japan           |  0.0010 |
|           Hungary          |  0.0012 |
|          Australia         |  0.0014 |
|           Canada           |  0.0014 |
|           Brazil           |  0.0014 |
|            Spain           |  0.0023 |
|           Poland           |  0.0035 |
|          Hong Kong         |  0.0059 |
|           Taiwan           |  0.0078 |

The slope values have been sorted in ascending order. Most of the countries shown in the table above (17 out of 22) have had an overall increase in the female share over these past decades. Although they do no show a strong increase, it is still great to see that for many countries, the presence of women on screen is growing.
However, India, the Netherlands, Sweden and especially Mexico and Bangladesh tend to have cast less and less women (compared to men) over the years.

Most of these regressions had relatively low $R^2$ values. This was to be expected as there most likely are many confounders and the variation of the female share index cannot be simply explained by the year the movie was released. However, as we are not interested in making precise predictions but rather at identifying the general underlying trend, this simple regression is enough. As it can be seen in the following figures, the regression line approximates well the overall trend. The countries that were plotted are the USA and India as they are the most predominant film producers. In order to have a better vizualisation of the 'extreme' slopes, we also decided to plot Taiwan (high increase) and Mexico (high decrease).

**PLOTS REGRESSIONS [USA, India, Taiwan, Mexico]**


The same analysis was performed for the movie genres. The regressions yield the following:


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

Similarly to the countries, most of the movie genres show an increasing trend of the female share. However, as fit was also the case for most countries, the increase is very dull. The $R^2$ values were also generally small for the same reasons as stated above. The genres that were plotted were again frequent movie-genres (Action, Thriller):

**plot regression [Action, Thriller]**

Another interesting observation that can be pointed out is that all genres for children (Children's, Children's Fantasy and Children's/Family) has seen a steady increase of the female share: 

**plot regression [Children's, Children's Fantasy and Children's/Family]**

This result is rather encouraging as the assimilation of stereotypes, such as "women are weak and men are strong" that are often portrayed in movies, begin at a very young age. Childhood is a particularly sensitive time in gender identity development. If children grow up watching movies with strong female protagonists, they are most likely to have reduced gender-based stereotypes. (REFERENCE!!! https://link.springer.com/article/10.1007/s11199-020-01127-z)


### Observational study: for similar careers, do actors participate in more movies than actresses?

Many confounders could potentially affect the number of women in movies. As an example, a man screenwriter is more likely to write a script with a more men-dominated point of view and hence cast more men as if the script was written by a woman. In order to try and mitigate the effect of confounders, a 1-on-1 matching observational study was performed based on these matching criteria: year of the actor's first movie, age of the actor for its first movie, age of the actor for its last movie, career length and ethnicity of the actor. Based on these criteria, an actor and an actress were matched and the number of movies they participated in were compared. As the distribution of the number of movies is heavy tailed, the natural logarithm of the movie count was used. It yileds the following result:

**barplot observational study**

From the plot above it seems that men and women with similar careers do play, on average, in the same amount of movies. A simple t-test allows to verify that observation. The t-test between the two averages gives a p-values = 0.96 which clearly shows that the null hypothesis (the two samples have identical averages) cannot be rejected.


### What are the predictors of the female share in a movie?

Through this analysis, we will try and identify what predictors in a movie would lead to a higher female share. We will use all of the information given for each movies: year when the movie was released, runtime, boxoffice and genre (only the top 10 genres were used). As most of the movies produced come from the USA, the analysis will only be carried out on movies made in the United States. After creating dummy variables for the 10 genres (categorical data), each predictors were standardized using z-scores in order to have comparable units. The results of the linear regression is summarized in the following table:

**Mettre tableau du summary de la linear regression**

The low $R^2 \approx 0.1$ values suggests that the predictors used do not explain all of the variance. Even though that number is reltively low, the p-values of our parameters are almost all significant (<0.05, despite the intercept and 'World cinema' genre), suggesting that they are significant for the assessment of the female share. In order to have a better visulization of the relative impact of each predictor on the female share, let's take a look at the following figure:

**plot de linear regression **

The way to interpret this figure is the following: when all other predictors take mean values, an increase in movie runtime of 1 standard deviation, leads on average to a decrease of 0.12 of the female share (VERIFIER CA AVEC LES AUTRES!!!!!!!!!). 

As it was already discovered in previous analyses, for the USA, the female share increases with time. The same result has been found using this linear regression. Some other intersting results are worth mentioning. As the stereotype suggests, love and romance is usually more associated to women than men. This stereotype is confirmed in this regression: romance movies are predictors of an increase in female share. On the other extreme, as the stereotypes go, men a more physical, adventurous and courageous. This is again confirmed in the figure above, with action movies being a strong negative predictor of female share.

### Conclusion of part 1 (quantitative analysis)

For most countries and genres, the female share index is slowly increasing, meaning that we are very gently arriving to men and women parity in movies (at least in numbers, even though we are not there yet!).

The information given in this observational study suggests that men and women with similar careers, play in the same number of movies. However, the analyses performed in this section do not give information about the type of roles the actors/actresses played (main or secondary roles). It is possible that in a movie with the same number of women and men cast, actors play dignifying roles whereas women play secondary, more demeaning roles. The second part of the data story will explore the qualitative inequalities.

Although the female share is slightly increasing from year to year, the typical stereotypes are still very strong (with women being part of more 'feminine topics' such as love and romance whereas men part of adventure/action movies). These inequalities may also be caused by other confounders (from which we have no data). As an example, a study analysing the inequalities in 1'300 popular films (REFERENCE https://assets.uscannenberg.org/docs/aii-inequality_1300_popular_films_09-08-2020.pdf), suggests that, as of September 2020, only 19.4% of screenwriters were women. Parity in screenwriters may also automatically lead to parity in gender representations in movies.



