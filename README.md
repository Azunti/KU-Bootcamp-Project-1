# KU-Bootcamp-Project-1
Project 1 Team 3 for KU Bootcamp with Caitlin Moran

Overview:
This project's hypothesis is that our three data sources have different biases and thus will have different top songs.
Thus our null hypothesis that we seek to disprove is that all three sources should have similar values
Our three data sources are: Billboard Hot 100 Dataframe, Rolling Stone Top 500 Dataframe, and Spotify API

Cleaning:
First we cleaned our two dataframes. 
[jp_spotify.ipynb.ipynb] contains the cleaning for Rolling Stone from [2021_list_raw] in the [Data] folder into [clean_bb_500] in the same folder. Since we were dealing with a dataset of 100 for Billboard, we limited the Rolling Stone set to 100 from the 500 it had. Of note: [jp_spotify.ipynb.ipynb] contains a few other items about this dataset we will discuss further below).
In the [Billboard Hot 100] folder, [billboard_cleaning] takes [Hot100base] and cleans that dataframe into [tocm_rank]. In this case, we determined that since a few hundred thousand songs had hit #1 on the chart, the most useful data would be how long the song was on the chart, and thus rated them by "tocm" or "time on chart max."

Surprise in Learning:
We initially doubted the results of [billboard_cleaning] as the top songs were songs we had not heard of before. However, by verifying the code was errorless, listening to the songs and connecting them with TikTok trends, and some additional research into the songs, we found that it made perfect sense for these songs to be at the top. Interestingly enough, this led us to realize we were experiencing our own biases. In this way, we unexpectedly expanded upon our hypothesis.

Initial data maniupulation:
In [jp_spotify.ipynb.ipynb] and [billboard_decade], we wanted to look at a quick proof of concept to see how different the data was before pulling in Spotify, so we manipulated the data to show us two graphs on decade of release of the song. Since this was even more different than we expected, we decided to include this in our final presentation as well.
Additionally, you can find in [jp_spotify.ipynb.ipynb] a scatterplot on release year vs rank, but we found the data inconclusive

Question Two - Top Artist:
At this point we started having roadblocks with the API which created a delay in answering questions 1 and 3. We moved onto question 2 in the meantime. Unfortunately we did find that Rolling Stone did not have a repeat artist, but in [billboard_artist], there is a bar graph of all artists appearing more than once on the list.

Question One - Top Genre:
At this point we were able to get the API working so we could pull Spotify genre and popularity data. In [BBHot_100_API] and [Rollingstone_500_API] we take our two cleaned dataframes and populate them with the API. In both you can see bar graphs of the top 10 genres for each list. These updated dataframes were both exported into the [Data] folder for use on question three as [RSwAPI] and [BBwAPI].

Question Three - Popularity
In [API_Popularity], data from [RSwAPI] and [BBwAPI] were pulled in. Then [RSvS] and [BBvS] were created to illustrate via scatter plot just how different the Spotify Popularity value was to the two dataframes.

Final Product
Our presentation is listed as [Song Popularity PowPoint] and our figures in [output_data]. Additionally you are reading the README.
In the end, we were able to overwhelmingly disprove the null hypothesis. Each dataset had its own biases and did not provide consistent information.




