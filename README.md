# ada-2021-project-lejt
ada-2021-project-lejt created by GitHub Classroom
DataShot
Public perspective on gun ownership and violence in relation to gun shooting events over time.
 
 
 
Abstract:
 
Gun ownership and regulation is a very divisive topic in the United States. It is clear that the country faces a problem with gun violence, this is reflected by the yearly 14 000 deaths following gun related homicides (statistic for 2019). However, people’s opinions over how this problem should be tackled differ greatly.
 
In the case of our project, we basically want to know :
“Who is thinking what and when?”.
 
This includes, political shifts in opinion, the differing impacts of shooting event types in the public eye, and the temporal evolution of public opinions.
 
We wish to include an external dataset containing shooting events information and cross-reference with the QuoteBank dataset to see how given events influence what is said publicly, and how much these events take over the press.
 













Research questions:
 
How do general opinions in the media shift following gun shooting events?
How does the political sphere, and the opinion of significant public figures, evolve in relation to gun shootings?
 

Proposed additional dataset:
 
US gun violence events archive:
https://www.gunviolencearchive.org/
 
The gunviolencearchive website provides various datasets that regroup shooting events into categories : Mass shootings by year, officer involved shootings, accidental death involving teen or children.
 
The datasets are csv files containing the following categories :
Incident ID, Incident Date, State, City or County, Address, Number killed, Number injured.
 
The length of the dataset should not be a significant concern as the csv file contains only 155 KB of information. We expect to be able to treat it within a Panda’s DataFrame.
 
 
 
 




Methods:
 
The first step of the project is to import the Quotebank dataset as well as the gun violence related dataset into  2 separate DataFrame for further analysis. The quotes will have to be filtered over a set of key-words that relate to gun violence, such as: gun, 2nd amendment, shooting, … .  We will also have to filter out incomplete and meaningless quotes – this could be done by removing quotes shorter than a certain word count threshold. For the gun violence dataset, we will select a subset of events and create different categories for these events (officer related, mass shooting, accidents).
 
We will need to identify whether the person quoted is sharing a positive or negative opinion with respect to gun ownership. Sentimental analysis will be applied to quotes to see whether they are pro 2nd amendment/ in favour of gun ownership, or against. There already exist numerous sentiment classification algorithms online which could be imported and used for the purpose of the project. One idea could be to use a natural language processing (NLP) model like BERT in combination with PCA to obtain a two dimensional output. Quotes than cannot be easily classified will be eliminated (for example, if we use an algorithm which outputs a positivity score ranging from 0 to 1, we could filter out all quotes with scores between 0.4 and 0.6).
 
Our aim is for each data entry from Quote Bank to be reduced to: speaker, date and sentimental score.
 
We will use the date category to cross-reference the shooting events with the relevant quotations within a given timeframe. This means, choosing quotes within a certain window of a shooting event.
 
We can plot the sentimental score of all quotes against time and observe the evolution of opinion. We can also add labels on the time axis for dates corresponding to significant shooting events (high death toll for example).
We can also select a few significant speakers who reoccur over the entire time frame of our dataset and plot their individual opinion evolution (or lack there-of).
 
Further analysis will be decided based on the results. We might explore the following supplementary questions …
 
How do different types of shooting events (officer involved, accident, mass shooting, …) affect public opinion, and which type matters most in the public eye?
 
What was the dialogue of Republican leaders with respect to gun violence and legislation before and after the 2016 election, specifically following mass shooting events?
 
 








Proposed timeline & organisation within the team:
 
Up to the 3rd December :
We will conduct the sentimental analysis and see whether the analysis described above yields any significant results.
 
Two members will work on the sentimental analysis while the other two will work on the plots.
 
Up to the 10th December:
Further analysis and eventual supplementary questions.
 
Up to the 17th December:
Develop and write the story… (prepare to be dazzled!)
