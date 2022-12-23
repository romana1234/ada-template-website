---
layout: default
---

# Part 2: Stereotypes and representation of different genders in the movie industry
If you have read part 1, we have good news: this part is not about numbers and statistics anymore - so, let's move on! If you have not read part 1 yet, you should - it is really interesting ;)

This part focuses on how female and male characters are portrayed in movies. We examine whether the stereotypes mentioned in the introduction are actually reflected in the movies. Analyses are conducted to investigate the qualitative inequalities between men and women in the movie industry. In addition, the evolution of the representation of different genders in different time periods is examined. 

For the stereotypes, already processed data are analysed. For the rest, the lexicon describing the genders is obtained through the summaries of the 42'306 movies. Each character of a certain movie is attributed to the words in the sentences he appears in. The characters are assigned the gender of the actor playing it, then the data are aggregated by gender.

## Stereotypes of characters in movies by gender
In the introduction, the most common stereotypes are already presented. As a reminder, the words used in the TV tropes for men and women, respectively, are shown in the word clouds below. All 500 instances of character types are included, and the font size of the words reflects the frequency of occurrence of that word.

We provide, nevertheless, two more numbers here: 69 of all instances represent a female character, while 431 refer to a male character. A bit unequal, isn't it?

![tvtropes_wordcloud](https://user-images.githubusercontent.com/114232327/209007228-546626e2-7177-4a72-95ab-766a2d4c6644.png)

Apart from the fact that the men icon is richer in words, we can also notice great differences in the meaning of the words. Nouns describing men are: guy, hunter, hero, badass, psycho. Nouns for women, on the other hand, are: girls, beauty, donna. This already indicates the man to be the strong and bad hero, while the female character is more beauty-oriented. These tendencies are even more highlighted when we look at adjectives. Female characters are dumb, brainless and blonde. Male characters are crazy, corrupt, evil, and so on.


## Words used to describe male and female characters
Now we really dig into the vast variety of male and female characters extracted from the 42'306 movie summaries. For every summary, the information about a character is extracted and divided into part of speech (adjectives, nouns and verbs). First, we analyze every parts of speech for each gender separately. This is shown by the word clouds below. For the third column, the words in the corresponding row are fed into the Empath library, so that they are assigned to different categories. In this way, the words for women can be compared to those for men. In this figure, we selected the five categories that show the largest difference between men and women for the corresponding part of speech.

![JJ_NN_VB_cat_diff](https://user-images.githubusercontent.com/114232327/209007446-ebce514e-011a-4ef8-a153-c28d0140f655.png)

Looking at the adjectives, significant differences between the two genders are in the Empath-categories children, youth, attractive, sexual and beauty. All these categories show a significantly higher contribution of female characters than males. Indeed, we see for example the big word 'young' for women, which explains the category 'youth', whereas the adjective 'old' is often used for describing both genders. The differences in the category 'children', can partly be explained by the adjective 'pregnant' that is quite often used for females, and obviously not in the adjectives describing male characters. \
The same tendencies are observed when looking at the nouns. Children, family, home and friends seem to be more important in the nouns attributed to female characters. Additionally, we observe the word 'love' that appears in the cloud of women quite big compared to its size in the cloud for men. \
Finally, for the verbs, we see a completely different graph. The most difference is detected in the categories related to violence, where verbs attributed to male characters have a much higher share than for women.


## Evolution of the representation of gender over time
Do we see a change in the portrayal of men and women when looking at different time periods? For the classification of words into Empath-categories, we used adjectives, nouns and verbs together.

Three time periods (P) are defined for this analysis:
* P1:         movie release year < 1950
* P2: 1950 <= movie release year < 1980
* P3: 1980 <  movie release year

Correlation between genders and time periods are given in the following matrix:

![corr_periods_gender](https://user-images.githubusercontent.com/114232327/209010234-a1d60ec9-0254-4696-90c7-042561da8cee.png)

We see a lower correlation between the genders (darker squares on the top right and bottom left). Very high correlation exists among the three periods of the same gender (green squares). We observe for both genders that P2 is more strongly correlated with P1 and P3 than the correlation between P1 and P3. In fact, the correlation coefficient for P2 and P3 is highest within the same sex.


### Principle component analysis (PCA)
A PCA allows us to represent the high number of features (Empath-categories) in some principle components (PCs). Therefore, we hope to show the differences in gender and in the three time periods on one single 2D graph! The two PCs with their respective explained variance ratio are depicted in the following figure. 

![PCA](https://user-images.githubusercontent.com/114232327/209010620-b254b5d5-e00b-45dd-97d9-4e61945340aa.png)

The PCA allows the discimination of the data based on two principles components. It seems that:
* PC I: separates men and women
* PC II: reflects differences in time periods

Overall, there seems to be a tendency for males and females to converge (both approach the midline when looking at the horizontal shift between time periods, especially on the male side). This regrouping suggests that the differences in the lexis used to describe each person's actions are smaller today. However, it is not clearly evident that women's vocabulary has changed more over time. These are however only hypotheses, PCA is not an appropriate method to confirm them. The sum of PC explained variance is 92.5%, which is considered satisfactory.



### Evolution of some empath categories over time

![evolution_categories](https://user-images.githubusercontent.com/114232327/209010664-a3564c56-3e8b-4328-9cd7-80b564038725.png)

  
Digging into specific categories of words evolution allow further investigations and analyses. Love category is mainly assigned to female, but this tendency is reducing since 1950. Crime is always more associated to men, although women words also have a high share in that category. Domestic work, which is still mainly associated with women characters, have some rises in men lexicon too. Power and heroic shows same chronological trends for both gender, even if they are still mainly associated to men. The relative share of words in the category leader is stable on a high level for men, whereas it decrased from P1 to P2 for women and now slightly increases again. Social media shows a high rise during the last period, which reflects the fact that social media is a more recent phenomenon. Finally, beauty has always been more important in the female vocabulary, with a peak in P2 for both gender a slighth decrase since then. 

### Limitations of the analysis on lexicons from film summaries:

As the lexicon is based on sentences where a character appears and do not consider how the character is implied, there are some biases. Also, the lexicon is not representatives of the subjectivity involved in the sentences. For example, a sentence where the word "tortured" is implied could be of different meaning. Having tortured sentiments or beeing tortured is absolutely not the same. Indeed, the categorisation done with empath would lead to the same category attribution for both meaning.


