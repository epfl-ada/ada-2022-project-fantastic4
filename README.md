# MovEquality

## Abstract :memo:
_Movies are often criticized for not accurately representing the population. For example, historically, most movie characters have been male. The women that are present are shown mainly in stereotyped roles such as housewives and secretaries. The goal of this project is to look at diversity in movies over time and see how it influences a movies success using the CMU Movie Summary Corpus. The first step is to analyze the diversity in the movies, focusing primarily on gender. The next step would be to analyze how people are represented. This would be done using sentiment analysis on the mentions of characters in the plot summary to see whether specific groups are portrayed in a more positive/negative light than others. Finally, we will take all of this into account when trying to establish if what we learned influences the rating as well as revenue of a movie._

## Research Questions :grey_question:
- **Question 1:** How diverse are the actors in movies? (Focus on gender) How has this evolved over time? Does it change depending on genre? Movie language/place?
- **Question 2:** Are the mentions of different characters more positive? What words are associated with male/female characters?
- **Question 3:** Can we use what we learned in the previous questions to make any connection to the success of a movie?

## Additional Datasets :file_cabinet:
- To enrich our CMU dataset, we decided to use the IMDb dataset containing information on about 50’000 movies. The advantage of this dataset is that it contains user ratings. But the IDs do not match the Wikipedia or Freebase IDs, which means that to merge these two datasets, we will have to match movies according to their title, which might lead to some matching mistakes. To avoid this, we will use the movie release date as an additional marker. The IMDb dataset also contains all the different title versions of the movie in addition to the original title, so we could compare the CMU movies title with all the title versions provided in the IMDb dataset and filter out the unnecessary datapoints. 
- Further, we discovered the “movie-stats” dataset on GitHub (https://github.com/danielgrijalva/movie-stats) that processed 6820 movies from IMDb dataset between 1986 and 2016 by adding information on budget of the movies, a vital piece of information, as it is a possible confounder for our 3rd Question. The issue with this dataset is that it is quite small and would thus reduce the amount of data we could work with.

## Methods :mag:
### Method Question 1
We will plot the evolution of the different distributions over time. We will be particularly careful on the period of aggregation in order to have significant results, and more generally the number of datapoints available per variable (e.g number of films per genre). Another important point will be to take care of potential confounders or interactions between variables. One such example is including the budget in the analysis.

### Method Question 2
In order to answer Question 2, we first lemmatize plot summaries and sort the sentences into groups that reference masculine or feminine pronouns. If a character name appears and is specified in the character dataset, the gender ot the actor playing it is also taken into account to put the sentence in a group. It is important to note that a sentence can appear in both categories if feminine and masculine pronouns/character names appear. We will then analyze the sentiments and words used in these two categories to observe the difference between them.
Below you can see the wordclouds with the words that are most ofen used in connection with female (left) and male (right) characters:

<p align="center">
  <img src="./Images/female_words.tiff" alt="most used words to decribe females" width="300"/>
  <img src="./Images/male_words.tiff" alt="most used words to decribe males" width="300"/>
</p>

### Method Question 3
To answer this question, we use both ratings and revenues as measures of success. Since revenue is biased by the time period and the movie’s budget, we will adapt the revenue over time by fitting a linear regression of the average or median revenues of movies, where x will be the time in years and y the average revenue. We will include movie budget, a potential confounder, in the regression model. We also need to enrich our CMU dataset with IMDb and movie stats to add ratings and budget respectively.
To relate the previous questions findings with this question, we can look at the revenue and rating relative to the positivity of their mentions of characters and depending on special features we might discover in question 1, we could relate them to the success of a movie.


## Proposed timeline :clock2:
- 25/11/22: Focus on homework 2 and preprocessing data done
- 02/12/22: **Homework 2 deadline**
- 02/12/22: Finish with data handling pipeline and data exploration
- 09/12/22: Website ready to be filled with our story and preliminary data story structure
- 16/12/22: All data handling and analysis done, after that we will focus on writing the data story and making it visually appealing on the website
- 23/12/22: **Project M3 deadline**


## Team Organization :raised_hands:

<table class="tg" style="undefined;table-layout: fixed; width: 342px">
<colgroup>
<col style="width: 164px">
<col style="width: 178px">
</colgroup>
<thead>
  <tr>
    <th class="tg-0lax">Teammate</th>
    <th class="tg-0lax">Tasks</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">:cat:</td>
    <td class="tg-0lax">Continue analyzing the dataset with respect to Question 3<br><br>Finish the merge the of the CMU dataset with additional datasets and explore these datasets<br><br>Take part in data story writing</td>
  </tr>
  <tr>
    <td class="tg-0lax">:unicorn:</td>
    <td class="tg-0lax">Continue analyzing the dataset with respect to Question 3<br><br>Produce the final data visualizations to be used on the website<br><br>Write the data story texts to communicate and explain the results<br><br>Write the README</td>
  </tr>
  <tr>
    <td class="tg-0lax">:bear:</td>
    <td class="tg-0lax">Continue analyzing the dataset with respect to Questions 2 and 3<br><br>Website for data presentation<br><br>Words clustering using NLP and initial visualizations<br><br>Sentiment analysis and creation of initial visualizations</td>
  </tr>
  <tr>
    <td class="tg-0lax">:fox_face:</td>
    <td class="tg-0lax">Continue analyzing the dataset with respect to Questions 1 and 3<br><br>Sentiment analysis and creation of initial visualizations</td>
  </tr>
</tbody>
</table>


## How to read the notebooks :file_folder:
There are two notebooks for this Milestone 2.
- _Handling of data.ipynb_: This notebook aims to load, clean, organize and pickle the data. As this notebook can take a while to run, we disabled some functions, and just printed the results.
- _Exploration of data.ipynb_: This notebook is meant for all future analysis. For now, it only contains the exploration of data. It uses the preprocessed data produced by the previous file.
