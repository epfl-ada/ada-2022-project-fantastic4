# MovEquality

## Abstract :memo:
_Movies are often criticized for not accurately representing the population. For example, historically, most movie characters have been male. The women that are present are shown mainly in stereotyped roles such as housewives and secretaries. The goal of this project is to look at diversity in movies over time and see how it influences a movies success using the CMU Movie Summary Corpus. The first step is to analyze the diversity in the movies, focusing primarily on gender. The next step would be to analyze how people are represented. This would be done using sentiment analysis on the mentions of characters in the plot summary to see whether specific groups are portrayed in a more positive/negative light than others. Finally, we will take all of this into account when trying to establish if what we learned influences the rating as well as revenue of a movie._

## Research Questions :grey_question:
- How diverse are the actors in movies? (Focus on gender) How has this evolved over time? Does it change depending on genre? Movie language/place?
- Are the mentions of different characters more positive? What words are associated with male/female characters?
- Can we use what we learned in the previous questions to make any connection to the success of a movie?

## Additional Datasets :fax:
_Which datasets ? Why ?_

## Methods :mag:
### Question 1
We will plot the evolution of the different distributions over time. We will be particularly careful on the period of aggregation in order to have significant results, and more generally the number of data available per variable (e.g number of films per genre).

Another important point will be to take care of potential counfounders or interaction between variables (e.g maybe there are more fantastic movies taking place in the U.S than in Europe).

### Question 2
### Question 3

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
    <td class="tg-0lax">Task 1<br><br>Task 2<br><br>Task 3</td>
  </tr>
  <tr>
    <td class="tg-0lax">:unicorn:</td>
    <td class="tg-0lax">Task 1<br><br>Task 2<br><br>Task 3</td>
  </tr>
  <tr>
    <td class="tg-0lax">:bear:</td>
    <td class="tg-0lax">Task 1<br><br>Task 2<br><br>Task 3</td>
  </tr>
  <tr>
    <td class="tg-0lax">:fox_face:</td>
    <td class="tg-0lax">Task 1<br><br>Task 2<br><br>Task 3</td>
  </tr>
</tbody>
</table>

<table class="tg" style="undefined;table-layout: fixed; width: 342px">
<colgroup>
<col style="width: 164px">
<col style="width: 178px">
</colgroup>
<thead>
  <tr>
    <th class="tg-0lax">Teammate</th>
    <th class="tg-0lax">:cat:</th>
    <th class="tg-0lax">:unicorn:</th>
    <th class="tg-0lax">:bear:</th>
    <th class="tg-0lax">:fox_face:</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Task</td>
    <td class="tg-0lax">Task 1<br><br>Task 2<br><br>Task 3</td>
    <td class="tg-0lax">Task 1<br><br>Task 2<br><br>Task 3</td>
    <td class="tg-0lax">Task 1<br><br>Task 2<br><br>Task 3</td>
    <td class="tg-0lax">Task 1<br><br>Task 2<br><br>Task 3</td>
  </tr>
</tbody>
</table>

# How to read the notebooks
There are two notebooks for this Milestone 2.
- _Handling of data.ipynb_: this notebook aims at loading, cleaning, organizing and pickling the data. As some this notebook can take a while to run, we disabled some functions, and just printed the results.
- _Exploration of data.ipynb_: this notebook is meant for all the future analysis. For now, it only contains the exploration of data. It uses the data saved by the previous file.
