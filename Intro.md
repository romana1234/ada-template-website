# Why do we care?

Gender equality is an extremely topical issue in today's world. Great efforts are being made to put women on an equal footing with men. However, there is still a lot to be done in many areas. But what is the situation in the film industry?

In recent years, the US movie industry has often been criticised in the media for its lack of female representation. As a simple and quick example: type 'most famous fictional adventurers' in a Google research bar. By clicking on the [first link provided](https://www.india.com/travel/articles/10-greatest-fictional-travelers-of-all-time-3236075/), a ranking of the top ten most famous fictional travellers of all time is shown, with only **one** being a woman. To extend this example, if you type most famous fictional characters, the first link [first link provided](https://fictionhorizon.com/most-iconic-fictional-characters/#:~:text=120%20Most%20Iconic%20Fictional%20Characters%20of%20All%20Time,Batman%20...%208%20Dorothy%20Gale%20...%20%C3%89l%C3%A9ments%20suppl%C3%A9mentaires) gives more than 120 characters, with only very few being women. In the [Wikipedia "Bechdel test" page](https://en.wikipedia.org/wiki/Bechdel_test#:~:text=The%20Bechdel%20test%20%28%2F%20%CB%88b%C9%9Bkd%C9%99l%20%2F%20BEK-d%C9%99l%29%20is,each%20other%20about%20something%20other%20than%20a%20man.) (a measure of the representation of women in film), the following graph was produced based on four different studies:

<img src="https://user-images.githubusercontent.com/100930184/209116724-4b221f87-53b8-49ae-b0d8-20f0f6fc92cc.png" width="700" />

This result clearly shows that the film industry is men dominated. But why is that such an issue one might ask? This lack of women representations has a large impact on our society, reinforcing the gender inequality of men doing great things (superhero, pilot, intelligent detective, scientist), and women being of secondary importance. As stated by [Bazzini et al., 1997](https://libres.uncg.edu/ir/asu/f/Bazzini_Doris_1997_The_Aging_Woman_in_Popular_Film.pdf): "Popular media images are reflections of a culture's attitudes, beliefs, and standards, as well as projections of desired realities [...] To the extent that consumers digest such material as truth, rather than fiction, the depictions laid forth by the media can be influential in the propagation and maintenance of stereotypes". In other words, what we see in movies is, to some extent, mirrored in real life.

Through this project, gender inequalities will be assessed in a quantitative and qualitative way.

**Note**: We want to make sure that we accept all different types of gender, and everyone should be able to live out the one they feel they belong to. However, since the only information we received in the data was whether the character was male or female, and those are the most common genders, we only examine those two genders.


# General overview of the data
In order to have a better feel for the data we are using, let's explore it by visualizing what we were given.

## Where does the data come from? 
The data from which our analysis is be based consists of 42'306 movie plot summaries extracted from Wikipedia, with release dates between 1880 and 2016. In addition to that, some movie metadata was also extracted from Freebase such as country, language, genre, characters, information about the actors/actresses playing the characters, movie runtime and release date.

## Who produces the movies and what are the most recurrent genres?

In the table below, the top 10 most movie-producing countries and frequently represented genres are displayed. In all of the movie datasets, almost 50% of all movies have been produced in the USA or India (out of 147 countries). The genres are more equally distributed. 


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

  


## When were the movies released? How much money did they generate? How long are they?

<img src="https://user-images.githubusercontent.com/100930184/209135056-d01d29b5-1cb8-40ab-bf99-d5d9492dca43.png" width="700" />

### Did you know that...

...most movies have a runtime of 100 minutes? Movie runtime has a mean of 94 and a median of 93 minutes, and 75% of movies have a runtime below 106 minutes. It is interesting to see that there are two peaks of runtime around 15 and 95 minutes.

For better visualisation, 45 movies were discarded to do the runtime histogram (those with runtime > 500 minutes). These outliers made the histogram difficult to read even on a log-log scale. They correspond to 0.07% of the movies in the dataset.

The movie boxoffice histogram has an x-axis on the log scale, given the wide range of values of boxoffice revenue, with a maximum of 2.78 billion dollars for "Avatar". Most revenues are concentrated around 5 million dollars.

For the movie release dates, this is clearly heavy-tail distributed, with an explosion of movies made since the 1980s.

## What are typical stereotypes regarding male and female characters in movies?

In their studies of "Learning Latent Personas of Film Characters", (Bamman et al., 2013) used a test set of 501 individual characters that are assigned to 72 character types. These character types are user-submitted examples of common tropes found, among other media, in television, movies, and fiction, coming from the website TV Tropes (http://tvtropes.org). \
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

But is it really as simple as that? This extremely stereotypical portrayal of male and female characters in the movie industry motivates us to examine the characters of the different genders in our collection of over 42000 movies. Are these stereotypes just clichés, or is there really something behind them? How has the representation of male and female characters changed over time? In "Part 2 - Qualitative Analysis", we explore these questions and find answers!
