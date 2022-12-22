---
layout: default
---

# Part 2: Stereotypes and representation of different genders in the film industry
If you have read part 1 we have good news: this part is no longer about numbers and statistics - so, keep on! If you have not yet read part 1, you should do it - it is really interesting ;)

This part focuses on how female and male characters are portrayed in movies. We examine whether the stereotypes mentioned in the introduction are actually reflected in the films. Analyses are conducted to investigate the qualitative inequalities between men and women in the film industry. In addition, the evolution of the representation of different genders in different time periods is examined. 

For the stereotypes, already processed data are examined. For the rest, the lexicons describing the genders is obtained through the summaries of the 42'306 movies. Each character of a certain movie is attributed the words in the sentences he appears in. The characters are assigned the gender of the actor playing it, then the data are aggregated by the gender.

## Stereotypes of characters in movies by gender
In the introduction, the most common stereotypes are already presented. As a reminder, the words used in the TV tropes for men and women, respectively, are shown in the word clouds below. All 500 instances of character types are included, and the font size of the words reflects the frequency of occurrence of that word.

We provide, nevertheless, two more numbers here: 69 of the 500 instances represent a female character, while 431 refer to a male character. A bit unequal, isn't it?

![tvtropes_wordcloud](https://user-images.githubusercontent.com/114232327/209007228-546626e2-7177-4a72-95ab-766a2d4c6644.png)

Beside the fact that the men icon is more rich in words, we can also obsereve huge differences in the meaning of the words. Nouns describing men are: guy, hunter, hero, badass, psycho. Whereas nouns for women are girls, beauty, donna. These already indicates the man to be the strong and bad hero, while the female character is more beauty-related. These tendencies are even more highlighted when we look at adjectives. Female characters are dumb, brainless and dumb. Male characters are crazy, corrupt, evil, and so on.


## Words used to describe male and female characters
Two versions -> I don't know which one is better...

For every part of speech (adj, vb, nn), the 5 empath categories are selected with the largest difference for men and women.
![JJ_NN_VB_cat_diff](https://user-images.githubusercontent.com/114232327/209007446-ebce514e-011a-4ef8-a153-c28d0140f655.png)




## Evolution of the representation of gender over time
(consider adjectives and nouns associated to a character)

Definition of three time periods (P):
* P1:         movie release year < 1950
* P2: 1950 <= movie release year < 1980
* P3: 1980 <  movie release year

Correlation matrix

![corr_periods_gender](https://user-images.githubusercontent.com/114232327/209010234-a1d60ec9-0254-4696-90c7-042561da8cee.png)



Very high correlation among the three periods of the same gender. Lower correlation between men and women. Highest correlation between P2 and P3 of the same gender (for both men and women).

### Principle component analysis (PCA)

![PCA](https://user-images.githubusercontent.com/114232327/209010620-b254b5d5-e00b-45dd-97d9-4e61945340aa.png)

  
The PCA allows the discimination of the data based on two principles components. PC I separates men and women. PC II: reflects differences in time periods. Overall there seems to be a tendency, especially on men side, of regroupement indicating less differences nowaday between the lexicon used to describe each characters actions. This is only an hypothesis, PCA is not a suitable method to confirm this. The PC explained variance ratio sum equal 92.5 %, which is considered as satisfactory.



### Evolution of some empath categories over time

![evolution_categories](https://user-images.githubusercontent.com/114232327/209010664-a3564c56-3e8b-4328-9cd7-80b564038725.png)

  
Digging into specific categories of words evolution allow further investigations and analyses. Love category is mainly assigned to female, but this tendency is reducing since 1950. Crime is always more associated
to men. Domestic work which is still mainly attributed to women characters have some rises in men lexicon too. Power and heroic shows same chronological trends for both gender, even if they are still mainly 
associated to men. Social media and science have also similar trends with first a cross over between the two first period and then a high rises for the last period. Finally, politics is less present in film summaries
than before, but the female share of this topic is disappearing. 

### Limitations of the analysis on lexicons from film summaries:

As the lexicons are based on sentences where a character appears and do not consider how the character is implied, there are some biases. Also, the lexicons are not representatives of the subjectivity involved
in the sentences. For example, a sentence where the word "tortured" is implied could be of different meaning. Having tortured sentiments or beeing tortured is absolutely not the same. Indeed the categorisation 
done with empath would lead to the same category attribution for both meaning.


