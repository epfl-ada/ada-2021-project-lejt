<h1 align="center"> DataShot </h1>

<h2 align="center"> Public perspective on gun ownership and violence in relation to gun shooting events over time.</h2>

<br/><br/>
#### Authors :

*Elie Graham , Justin Manson, Lorenzo Germini, Thibaud Martin*

Link to the website : [Datashot](https://thibmartin.github.io/Datashot/)

#### Abstract:

Gun ownership and regulation is a very divisive topic in the United States. It is clear that the country faces a problem with gun violence, this is reflected by the yearly 14 000 deaths following gun related homicides (statistic for 2019). However, people&#39;s opinions over how this problem should be tackled differ greatly.

In the case of our project, we basically want to know :

&quot;Who is thinking what and when?&quot;.

This includes, political shifts in opinion, the differing impacts of shooting event types in the public eye, and the temporal evolution of public opinions.

We wish to include an external dataset containing shooting events information and cross-reference with the QuoteBank dataset to see how given events influence what is said publicly, and how much these events take over the press.

<br/><br/>

#### Research questions:

How do general opinions in the media shift following gun shooting events?

How does the political sphere, and the opinion of significant public figures, evolve in relation to gun shootings?

<br/><br/>

#### Proposed additional dataset:

US gun violence events archive:

https://www.gunviolencearchive.org/

The gunviolencearchive website provides various datasets that regroup shooting events into categories : Mass shootings by year, officer involved shootings, accidental death involving teen or children.

The datasets are csv files containing the following categories :

Incident ID, Incident Date, State, City or County, Address, Number killed, Number injured.

The length of the dataset should not be a significant concern as the csv file contains only 155 KB of information. We expect to be able to treat it within a Panda&#39;s DataFrame.

<br/><br/>

#### Methods:

The first step of the project was to import the Quotebank dataset as well as the gun violence related dataset into 2 separate DataFrames for further analysis. The gun violence dataset was obtained from the following [website](https://www.gunviolencearchive.org/). The quotes have been filtered over a set of key-words that relate to gun violence, see below the list of keywords and their distribution across dataset.  We also have filtered out incomplete and meaningless quotes, by removing quotes shorter than a certain word count threshold. For the gun violence dataset, we selected a subset of events based on the number of deaths. We choose a threshold of 8 deaths by visually analyzing the graphs.

We needed to identify whether the person quoted is sharing a positive or negative opinion with respect to gun ownership. Sentimental analysis was applied to quotes to see wheter they display a positive or negative sentiment. Furthermore, we performed emotional analysis to see the evolution of particular emotions, namely fear, anger, sadness, agression, joy, optimism. There already exist numerous sentiment classification algorithms online which are available and we needed to select the best ones for the purpose of the project. We settled on Vader and Bert. Finally we classified the quotes in 3 categories: positive, neutral or negative, based on their score. We also chose to apply emotion analysis to observe the evolution of different emotions around gun shootings events.

The website (link on top of file) will present our work and our final analysis.


#### Proposed timeline &amp; organisation within the team:

Up to the 3rd December :

We had to rework on the filtering of the dataset, as it was deemed too scarce after milestone 2, we also split the tasks between the team members.

Up to the 10th December:

We took care of the bulk of the analysis separately and started working on the data story.

Up to the 17th December:

We finished the analysis and finalised the data story on the website.

###### Work repartition
Justin : Worked on data filtering, LDA and Emotion extraction
Lorenzo : Worked on Sentiment Analysis (Bert and Vader), as well as data filtering
Elie: Worked on correlation between events and multiple plots
Thibaud: Worked on data filtering and data story
