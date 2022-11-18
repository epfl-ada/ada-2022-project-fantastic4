# MovEquality

## Abstract :memo:
_Movies are often criticized for not accurately representing the population. For example, historically, most movie characters have been male. The women that are present are shown mainly in stereotyped roles such as housewives and secretaries. The goal of this project is to look at diversity in movies over time and see how it influences a movies success using the CMU Movie Summary Corpus. The first step is to analyze the diversity in the movies, focusing primarily on gender. The next step would be to analyze how people are represented. This would be done using sentiment analysis on the mentions of characters in the plot summary to see whether specific groups are portrayed in a more positive/negative light than others. Finally, we will take all of this into account when trying to establish if what we learned influences the rating as well as revenue of a movie._

## Research Questions :grey_question:
- How diverse are the actors in movies? (Focus on gender) How has this evolved over time? Does it change depending on genre? Movie language/place?
- Are the mentions of different characters more positive? What words are associated with male/female characters?
- Can we use what we learned in the previous questions to make any connection to the success of a movie?

## Additional Datasets :fax:
To enrich our CMU dataset, we considered using the IMDb dataset containing information about 50’000 movies. The advantage of this dataset is that it contains ratings from users which we do not have with the CMU dataset. But this dataset presents some challenges: the IMDb movie IDs do not match the Wikipedia or Freebase IDs, which means that to merge these two datasets, we will have to match movies according to their title, which might lead to some matching mistakes if different movies have the same title or if the same movies were registered in the dataset with different titles. To partially counter this, we considered using the movie release date in addition to compare if movies are matching. Also, the IMDb dataset contains all the different title versions of the movie in addition to the original title, so we could compare the CMU movies title with all the title versions provided in the IMDb dataset.
Further, we discovered the “movie-stats” dataset on GitHub (https://github.com/danielgrijalva/movie-stats) that processed 6820 movies from IMDb dataset between 1986 and 2016 by adding information on budget of the movies when known, an information that we are looking for to answer our third research question dealing with movies success. The issue with this dataset is that it contains only about 7000 movies so it will considerably reduce our original dataset. 


## Methods :mag:
### Question 1
We will plot the evolution of the different distributions over time. We will be particularly careful on the period of aggregation in order to have significant results, and more generally the number of data available per variable (e.g number of films per genre).

Another important point will be to take care of potential counfounders or interaction between variables (e.g maybe there are more fantastic movies taking place in the U.S than in Europe).

### Question 2
In order to answer Question 2, we first lemmatize plot summaries and sort the sentences into groups that reference masculine or feminine pronouns. If a charater name appears and is specified in the character dataset, the gender ot the actor playing it is also taken into account to put the sentence in a group. It is important to note that a sentence can appear in both categories if feminine and masculine pronouns/actor gender appear. 
We will then analyze the sentiments and words used in these two categories to observe the difference between them.

### Question 3
Definition of success: Rating and Revenue, how we adapted revenue over time and removed confounders such as movie budget
This is where we talk about adding more data to make our view more complete
Match the datasets on the title, add the freebase ID
Look at the revenue and rating relative to the positivity of their mentions of characters
We need to try to make a link with question 1 if we find anything interesting there
Compare positivity of character mention to rating of movie


## Proposed timeline :clock10:
- 25/11/22: Focus on homework 2 and preprocessing data done
- 02/12/22: Homework 2 deadline
- 02/12/22: Finish with data handling pipeline and data exploration
- 09/12/22: Website ready to be filled with our story and preliminary data story structure
- 16/12/22: All data handling and analysis done, after that we will focus on writing the data story and making it visually appealing on the website
- 23/12/22: Project M3 deadline


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


## How to read the notebooks
There are two notebooks for this Milestone 2.
- _Handling of data.ipynb_: this notebook aims at loading, cleaning, organizing and pickling the data. As this notebook can take a while to run, we disabled some functions, and just printed the results.
- _Exploration of data.ipynb_: this notebook is meant for all the future analysis. For now, it only contains the exploration of data. It uses the data saved by the previous file.
