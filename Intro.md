# test image

![alt text for image](../assets/img/movie_dates_hist.png)

# Why is it important ?

In recent years, the US movie industry has often been criticised in the media for its lack of female representation. As a simple and quick example: type 'most famous wizardess' in a Google research bar. Google automatically suggests 'most famous wizard' and not wizardess. By clicking on the [first link provided](https://faceoffdb.com/lists/powerful-wizards-and-witches/), a ranking of the top 45 most famous wizards/wizardesses is given with only **one** woman in the top 10. In the [Wikipedia "Bechdel test" page](https://en.wikipedia.org/wiki/Bechdel_test#:~:text=The%20Bechdel%20test%20%28%2F%20%CB%88b%C9%9Bkd%C9%99l%20%2F%20BEK-d%C9%99l%29%20is,each%20other%20about%20something%20other%20than%20a%20man.) (a measure of the representation of women in film), the following graph was produced based on four different studies:

**METTRE IMAGE "WIKI_"**

This result clearly shows that the film industry is men dominated. But why is that such an issue one might ask (hopefully not...)? This lack of women representations has a large impact on our society, reinforcing the gender inequality of men doing great things (superhero, pilot, intelligent detective, scientist), and women being of secondary importance. As stated by (Bazzini et al., 1997): "Popular media images are reflections of a culture's attitudes, beliefs, and standards, as well as projections of desired realities [...] To the extent that consumers digest such material as truth, rather than fiction, the depictions laid forth by the media can be influential in the propagation and maintenance of stereotypes". In other words, what we see in movies is, to some extent, mirrored in real life.

Through this project, the gender inequalities will be assessed in a quantitative and qualitative way.

PS: We want to make sure that we accept all different types of gender, and everyone should be able to live out the one they feel they belong to. However, since the only information we received in the data was whether the character was male or female, and those are the most common genders, we only examine those two genders.
-> I don't know if we want to write something like this??


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

## What are typical stereotypes regarding male and female characters in movies ?

(...) used a test set of 501 individual characters that are assigned to 72 character types. These character types are user-submitted examples of common tropes found, among other media, in television, film, and fiction, coming from the website TV Tropes (http://tvtropes.org). \
The following table shows the 10 most common TV tropes and the number of movies in which those tropes appear.

| tv trope                        | # of movies|
|:--------------------------------|:-----------|
| crazy jealous guy               |     25     |
| corrupt corporate executive     |     23     |
| byronic hero                    |     17     |
| psycho for hire                 |     16     |
| father to his men               |     15     |
| stoner                          |     13     |
| brainless beauty                |     12     |
| master swordsman                |     12     |
| dumb blonde                     |     11     |
| slacker                         |     11     |

So, in other words, we have:
* male character: crazy, corrupt, hero, stoner, ...
* female character: brainless, beauty, dumb, blonde, ...

which pretty much represent the classic clichés about men and women.

But is it really as simple as that? This extremely stereotypical portrayal of male and female characters in the film industry motivates us to examine the characters of the different genders in our collection of over 42000 films. Are these stereotypes just clichés, or is there really something behind them? How has the representation of male and female characters changed over time? In "Part 2 - Semantic Analysis" we explore these questions and find answers!
