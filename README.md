# MovEquality

Check out our [website](https://pierreancey.github.io/) to read our data story!

## Abstract :memo:
_Movies are often criticized for not accurately representing the population. For example, historically, most movie characters have been male. The women that are present are shown mainly in stereotyped roles such as housewives and secretaries. The goal of this project is to look at gender diversity in movies over time and see how it influences a movies success using the CMU Movie Summary Corpus. After the numbers were determined, the next step was to analyze how people are portrayed. This was done using sentiment analysis on the mentions of characters in the plot summary to see whether men are presented in a different light than women. Finally, we took all of this into account when trying to establish if what we learned influences the rating as well as revenue of a movie._

## Research Questions :grey_question:
- **Question 1:** How diverse are the actors genders in movies? How has this evolved over time? Does it change depending on genre? Movie language/place?
- **Question 2:** Are the mentions of different characters more positive? What words are associated with male/female characters?
- **Question 3:** Can we use what we learned to make any connection to the success of a movie?

## Additional Datasets :file_cabinet:
- To enrich our dataset, we decided to use the IMDb dataset containing information on about 50’000 movies, including user ratings. But the IDs do not match the Wikipedia or Freebase IDs, therefore, we will have to match movies according to their title, which might lead to some matching mistakes. To avoid this, we will use the movie release date as an additional marker. The IMDb dataset also contains all the different title versions of the movie, so we could compare the CMU movie titles with all the title versions provided in the IMDb dataset and filter out unnecessary datapoints. 
- Further, we discovered the “movie-stats” dataset on GitHub (https://github.com/danielgrijalva/movie-stats) that processed 6820 movies from IMDb dataset between 1986 and 2016 by adding information on budget of the movies, a vital piece of information, as it is a possible confounder for our 3rd Question. The issue with this dataset is that it is quite small and would thus reduce the amount of data we could work with considerably.

## Methods :mag:
### Method Question 1
We plotted the evolutions of several distributions over time to study the evolution of women's place in films. We also studied the differences between the movie genres, countries and languages. We also made sure to take care of potential confounders or interactions between variables. One such example is including the budget in the analysis.

These observations proved useful for question 3, as they gave us a glimpse of the trends and gave us more information on major confounders!

### Method Question 2
In order to answer Question 2, we first lemmatize plot summaries and sort the sentences into groups that reference masculine or feminine pronouns. If a character name appears and is specified in the character dataset, the gender of the actor playing it is also considered when categorizing the sentences. It is important to note that a sentence can appear in both categories if feminine and masculine pronouns/character names appear. We will then analyze the sentiments and words used in these two categories to observe the difference between them.
Below you can see the word clouds with the words that are most often used in connection with female and male characters.

To quantify this, we went through the movie summaries to find words that if they are found in a sentence the sentence has the highest possible probability to be male or female. Check out our data story to see the (unsurprising) results.

### Method Question 3
We first defined the success of a movie and used both ratings and revenues as its measures. Then, given everything we learned in the previous analysis, and the new data we obtained with the additional datasets, we performed a matching study to remove most confounding variables. Defining our control and treated groups, and constructing a distance between films, and finally matching the films, led us to very interesting conclusions. 

## Accomplished Tasks :raised_hands:

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
    <td class="tg-0lax">Alice :cat:</td>
    <td class="tg-0lax">Analyzed the dataset with respect to Question 3<br><br>Finished the merge the of the CMU dataset with additional datasets and explored these datasets<br><br>Took part in data story writing</td>
  </tr>
  <tr>
    <td class="tg-0lax">Bettina :unicorn:</td>
    <td class="tg-0lax">Analyzed the dataset with respect to Question 3<br><br>Produced the data visualizations on the website<br><br>Wrote the data story texts to communicate and explain the results<br><br>Updated the README</td>
  </tr>
  <tr>
    <td class="tg-0lax">Pierre :bear:</td>
    <td class="tg-0lax">Analyzed the dataset with respect to Questions 2 and 3<br><br>Made the website<br><br>Did the word clustering using NLP and made initial visualizations<br><br>Did the sentiment analysis and made initial visualizations</td>
  </tr>
  <tr>
    <td class="tg-0lax">Sam :fox_face:</td>
    <td class="tg-0lax">Analyzed the dataset with respect to Questions 1 and 3<br><br> Did sentiment analysis and made initial visualizations</td>
  </tr>
</tbody>
</table>


## How to Read the Notebooks :file_folder:
There are four notebooks for Milestone 3.
- _Handling of data.ipynb_: This notebook aims to load, clean, organize and pickle the data. It also merges the datasets. As this notebook can take a while to run, we disabled some functions, and just printed the results.
- _DataAnalysis.ipynb_: This notebook is meant for all analysis except NLP part. It contains all the studies corresponding to questions 1 and 3.
- _Handling NLP.ipynb_: This notebook prepares the data for the NLP analysis
- _Exploration NLP.ipynb_: This notebook contains all the NLP corresponding to question 2
- _Visualizations.ipynb_: This notebook contains the code to make the plots in our data story
