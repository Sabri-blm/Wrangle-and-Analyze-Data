<p align="center">
  <a href="https://www.udacity.com/">
    <img src='https://course_report_production.s3.amazonaws.com/rich/rich_files/rich_files/5511/s300/udacity-logo.png' alt="Udacity logo" width = 100px>
   </a>
</p>

<h3 align="center"><a href = "https://www.udacity.com/course/data-analyst-nanodegree--nd002"> Udacity Data Analyst Nanodegree </a></h3>
<h4 align="center">Project 2: Wrangle and Analyze Data</h4>


## Table of Contents
- [Project Overview](#project_overview)
- [Installation](#installation)
- [Project Details](#details)
  - [Gathering Data](#gather)
  - [Assessing Data](#assess)
  - [Cleaning Data](#clean)
  - [Storing, Analyzing, and Visualizing](#sav)
  - [Report](#report)
- [Project Motivation](#motivation)
- [Results](#results)
- [Licensing, Authors, and Acknowledgements](#licensing)

### 1.Project Overview <a name="project_overview"></a>

Real-world data rarely comes clean. Using Python and its libraries, you will gather data from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it. This is called data wrangling. You will document your wrangling efforts in a Jupyter Notebook, plus showcase them through analyses and visualizations using Python (and its libraries) and/or SQL.

The dataset that you will be wrangling (and analyzing and visualizing) is the tweet archive of Twitter user [@dog_rates](https://twitter.com/dog_rates), also known as [WeRateDogs](https://en.wikipedia.org/wiki/WeRateDogs). WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "[they're good dogs Brent](http://knowyourmeme.com/memes/theyre-good-dogs-brent)." WeRateDogs has over 4 million followers and has received international media coverage.

WeRateDogs downloaded their Twitter archive and sent it to Udacity via email exclusively for you to use in this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017. More on this soon.
<p align="center">
  <img src="https://video.udacity-data.com/topher/2017/October/59dd378f_dog-rates-social/dog-rates-social.jpg" width = 500px; height =300px;\>
</p>

### 2.What Software Do I Need? <a name="installation"></a>

The entirety of this project can be completed using the following:

<ul>
    <li>You need to be able to work in a Jupyter Notebook on your computer or Google Colab online.</li>
    <li>The following packages (libraries) need to be installed. You can install these packages via conda or pip.</li>
  <ul>
        <li>pandas</li>
        <li>NumPy</li>
        <li>requests</li>
        <li>tweepy</li>
        <li>json</li>
    </ul>
</ul>

### 3.Project Details <a name="details"></a>

The tasks in this project are as follows:
<ul>
    <li>Data wrangling, which consists of:</li>
  <ul>
        <li>Gathering data.</li>
        <li>Assessing data.</li>
        <li>Cleaning data.</li>
    </ul>
    <li>Storing, analyzing, and visualizing your wrangled data</li>
    <li>Reporting on 1) your data wrangling efforts and 2) your data analyses and visualizations</li>
</ul>

#### 3.1.Gathering Data for this Project <a name="gather"></a>

Gather each of the three pieces of data as described below:
<ol>
    <li>The WeRateDogs Twitter archive. I am giving this file to you, so imagine it as a file on hand. Download this file manually by clicking the following link: twitter_archive_enhanced.csv</li>

   <li>The tweet image predictions, i.e., what breed of dog (or other object, animal, etc.) is present in each tweet according to a neural network. This file (image_predictions.tsv) is hosted on Udacity's servers and should be downloaded programmatically using the <a href="https://pypi.org/project/requests/">Requests</a> library and the following URL: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv</li>

   <li>Each tweet's retweet count and favorite ("like") count at minimum, and any additional data you find interesting. Using the tweet IDs in the WeRateDogs Twitter archive, query the Twitter API for each tweet's JSON data using Python's <a href="http://www.tweepy.org/">Tweepy</a> library and store each tweet's entire set of JSON data in a file called <em>tweet_json.txt file</em>. Each tweet's JSON data should be written to its own line. Then read this .txt file line by line into a pandas DataFrame with (at minimum) tweet ID, retweet count, and favorite count. Note: do not include your Twitter API keys, secrets, and tokens in your project submission.</li>
</ol>

#### 3.2.Assessing Data for this Project <a name="assess"></a>

After gathering each of the above pieces of data, assess them visually and programmatically for quality and tidiness issues. Detect and document <strong>at least eight (8) quality issues</strong> and <strong>two (2) tidiness issues</strong> in your <em>wrangle_act.ipynb</em> Jupyter Notebook. To meet specifications, the issues that satisfy the Project Motivation must be assessed.

#### 3.3.Cleaning Data for this Project <a name="clean"></a>

Clean each of the issues you documented while assessing. Perform this cleaning in <em>wrangle_act.ipynb</em> as well. The result should be a high quality and tidy master pandas DataFrame (or DataFrames, if appropriate). Again, the issues that satisfy the Project Motivation must be cleaned.

#### 3.4.Storing, Analyzing, and Visualizing Data for this Project <a name="sav"></a>

Store the clean DataFrame(s) in a CSV file with the main one named <em>twitter_archive_master.csv</em>. If additional files exist because multiple tables are required for tidiness, name these files appropriately. Additionally, you may store the cleaned data in a SQLite database.

Analyze and visualize your wrangled data in your <em>wrangle_act.ipynb</em> Jupyter Notebook. <strong>At least three (3) insights and one (1) visualization</strong> must be produced.

#### 3.5.Reporting for this Project <a name="report"></a>

Create a <strong>300-600 word written report</strong> called <em>wrangle_report.pdf</em> or <em>wrangle_report.html</em> that briefly describes your wrangling efforts. This is to be framed as an internal document.

Create a <strong>250-word-minimum written report</strong> called <em>act_report.pdf</em> or <em>act_report.html</em> that communicates the insights and displays the visualization(s) produced from your wrangled data. 

#### All the files:

* All of the files are:
  * `wrangle_act.ipynb`: code for gathering, assessing, cleaning, analyzing, and visualizing data
  * `wrangle_report.pdf` or `wrangle_report.html`: documentation for data wrangling steps: gather, assess, and clean
  * `act_report.pdf` or `act_report.html`: documentation of analysis and insights into final data
  * `twitter_archive_enhanced.csv`: file as given
  * `image_predictions.tsv`: file downloaded programmatically
  * `tweet_json.txt`: file constructed via API
  * `twitter_archive_master.csv`: combined and cleaned data

### 4.Project Motivation <a name="motivation"></a>

This is an Udacity Nanodegree project. I was interested in using Tweet Data to better understand: </br>
- What type of device produces these tweets.
- What is the most popular dog breed.
- What is the most popular dogtionary term.

## 5.Results <a name="results"></a>
-  What type of device produces these tweets?</br>
This question is very easy to explore and answer because we already have the source column in the twitter_archive_mastered dataset. This mean that we can directly use the value_counts() methode to find the answer that we are looking for.
From the result we can see that 1845 people uses the iphone to tweet,25 are web clients, and 9 are using tweetdeck.

- What is the most popular dog breed?</br>
In this part, it is very interessting for us to know which dog breed is the favorite amoung ourdata because this could help us understand our data even more. using code we grouped thedata and then sort it to fi nd this result:
<p align="center">
  <img src="https://raw.githubusercontent.com/Abhishek20182/Wrangle-and-Analyze-Data/master/Result-2.png">
</p>
as we can see the golden retriever breed is the most favorite breed of dogs.

- What is the most popular dogtionary term?</br>
Just as the last question, knowing which dogtionary term is used could make understanding the dataset much easier, and visualizing it will make it even cleaner thats why we have :
<p align="center">
  <img src="https://raw.githubusercontent.com/Abhishek20182/Wrangle-and-Analyze-Data/master/Result-2.png">
</p>
here we see that the pupper term is the most used one out of the bunch which indicate according to the dogtionary that the favorite dogs are small, younger dogs are the favorites.

## 6.Licensing, Authors, Acknowledgements<a name="licensing"></a>
Must give credit to Udacity to providing this data. You can find the Licensing for the data and other descriptive information at [here](https://support.twitter.com/articles/20170160)
