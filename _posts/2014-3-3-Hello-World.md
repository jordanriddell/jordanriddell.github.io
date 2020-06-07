---
layout: post
title: Twitter Data
---

 <div class="entry">
    {{ 
This post will detail how to use a windows command prompts and Python to scrape Twitter data for a single user account and then explain how to organize and visualize tweets, retweets, likes data.

![_config.yml]({{ site.baseurl }}/images/config.png)

First, make sure to have at least Python 3 on your computer. Next, you will need to have pip installed on your pc. Once those are both completed, go to [Nickersen Weng's github](https://github.com/NicksonWeng/Get-Old-Tweet-Modified) and download the files from the repository to a folder of your choice. Just remember where you save and extract them because you will need to set the path directory to the same folder as those files later on.

Using the Windows command prompt (just type cmd in the search bar on the bottom left), enter the following commands in sequence.

#Any line with # is comment, rest is entered at end of directory and after the>
#first, make sure pip has been installed on your device

#check to make sure you have python
python

#exit python environment
exit()

#set working directory to the Twitterdata folder that you have the unzipped files in
cd Dropbox\Twitterdata

#install GetOldTweets3
python -m pip install GetOldTweets3

#execute Twitter search and download - multiple options
#keyword search example: python Exporter.py --querysearch "Keyword Here" --since YEAR-MM-DD --until YEAR-MM-DD --maxtweets XXX --output filename.csv
#notes: keyword may be case sensitive; since = start date; until = end date
#username search: python Exporter.py --username "username" --since YEAR-MM-DD --until YEAR-MM-DD --maxtweets XXX --output filename.csv
#notes: username may be case sensitive and should include all characters after the @; since = start date; until = end date

#I used the following command to download all tweets from the Dallas Police Department's Twitter account. Note: if you do not want all tweets, restrict the date or set a maxtweet limit.
python Exporter.py --username "DallasPD" --since 2009-04-01 --until 2020-06-06 --output dpd_tweets.csv
}}
  </div>

The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.
