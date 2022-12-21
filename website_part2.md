---
layout: default
---

# Part 2: Stereotypes and representation of different genders in the film industry
This part focuses on how female and male characters are represented in movies. Typical stereotypes are identified and analyses are performed, if they are really reflected in the movies. Furthermore, the evolution of the representation in time is examined. 

For the stereotypes, already processed data are examined. For the rest, the lexicons describing the genders is obtained through the summaries. Each character of a certain movie is attributed the words in the sentences he appears in. The characters are assigned the gender of the 
actor playing it, then the data are aggregated by the gender.

## Stereotypes of characters in movies by gender
72 character types drawn from tvtropes.com, along with 500 instances of those types

of which 69 refering to a female actor, and 431 to a male actor

10 most prevalent character types:

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


Image with words from tv tropes by gender

![tvtropes_wordcloud](https://user-images.githubusercontent.com/114232327/208700236-9934b814-e310-44bc-9c21-f3f5868def30.png)


The most used words in these tv tropes for characterizing a female and a male character respectively depict pretty much the stereotypes: The beautiful, blonde and dumb girl, whereas male characters are represented among other as corrupt, a badass, a hero. Moreover, the most used noun for women is "girl", while "guy" is mostely used to represent a man.

## Words used to describe male and female characters
Two versions -> I don't know which one is better...

For every part of speech (adj, vb, nn), the 5 empath categories are selected with the largest difference for men and women.
![JJ_NN_VB_cat_diff](https://user-images.githubusercontent.com/114232327/208700451-e087f8ed-c867-43a4-a19d-70cedbd76b84.png)

Version 2: 4 fixed empath categories are selected and we look at their values for every part of speech.
![JJ_NN_VB_cat_fix](https://user-images.githubusercontent.com/114232327/208700473-ef5d540a-817c-4d9f-a301-bcde2c4c307d.png)



## Evolution of the representation of gender over time
(consider adjectives and nouns associated to a character)

Definition of three time periods (P):
* P1:         movie release year < 1950
* P2: 1950 <= movie release year < 1980
* P3: 1980 <  movie release year

Correlation matrix
![corr_periods_gender](https://user-images.githubusercontent.com/114232327/208702863-5bea998b-accb-4f68-bd17-9d59bf2a5b47.png)



Very high correlation among the three periods of the same gender. Lower correlation between men and women. Highest correlation between P2 and P3 of the same gender (for both men and women).

### Principle component analysis (PCA)

![PCA](https://user-images.githubusercontent.com/114232327/208701868-6bbcbefa-504b-47ad-a21c-536df850fe5c.png)

The PCA allows the discimination of the data based on two principles components. PC I separates men and women. PC II: reflects differences in time periods. Overall there seems to be a tendency, especially on men side, of regroupement indicating less differences nowaday between the lexicon used to describe each characters actions. The PC explained variance ratio sum equal 92.5 %, which is considered as satifactory.



### Evolution of some empath categories over time

![evolution_categories](https://user-images.githubusercontent.com/114232327/208702776-a7bb9f11-504e-4eea-a1ad-412ad2ea5328.png)


