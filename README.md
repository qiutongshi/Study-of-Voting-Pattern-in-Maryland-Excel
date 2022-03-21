# Rep-Dep-Maryland

## Background
The 2020 presidential election is coming soon. The results of the 2016 presidential election came as a surprise to nearly everyone who had been following the national and state election polling, which consistently projected Hillary Clinton as defeating Donald Trump. Relying largely on opinion polls, election forecasters put Clinton’s chance of winning at anywhere from 70% to as high as 99%, and pegged her as the heavy favorite to win a number of states such as Pennsylvania and Wisconsin that in the end were taken by Trump.

There are many reasons as to why polling failed during the election. One speculation was that Trump’s supporters were harder to reach, and that mainstream media and industries such as Hollywood and High-tech favored Clinton significantly more. Some have also suggested that many of those who were polled simply were not honest about whom they intended to vote for. The idea of so-called “shy Trumpers” suggests that support for Trump was socially undesirable, and that his supporters were unwilling to admit their support to pollsters. This hypothesis is reminiscent of the supposed “Bradley effect,” when Democrat Tom Bradley, the black mayor of Los Angeles, lost the 1982 California gubernatorial election to Republican George Deukmejian despite having been ahead in the polls, supposedly because voters were reluctant to tell interviewers that they were not going to vote for a black candidate.

This project would use cluster analysis to group voters who were registered as  a Republican in Maryland the 2016 presidential election to see whether their activity during participation in the poll and voting would be similar to the ["shy Trumpers hypothesis"](https://www.npr.org/2016/11/14/502014643/4-possible-reasons-the-polls-got-it-so-wrong-this-year). 

## Business Question
Are voting patterns of Democrats or Republicans in Maryland disturbed by community or mainstream media pressure?

## Data Question
How active are Democrats and Republicans voters in Maryland by counties? What are the voting patterns of Democrats and Republicans in Maryland?

## Data Metrics
- Polls number: The number of people participating in an opinion poll about the election.
- Early Voting number: The number of people voted early is an indicator of voter engagement. 
- Absentee Voting number: An absentee ballot is a vote cast by someone who is unable or unwilling to attend the official polling station to which the voter is normally allocated. Can be a weak indicator for people that are not comfortable with going to a station and vote because of political reasons. 
- Provisional Voting number: The number of people who may be eligible for voting, but eventually the provisional ballot may not be counted at the local board of election’s discretion.
- Voter Turnout: The percentage of eligible voters who cast a ballot in the election. 

## Data Sources
[Maryland the State Board Election: 2016 Presidential Election](https://elections.maryland.gov/elections/2016/index.html)

## Data Analysis
This project uses 3-cluster analysis for each party in Maryland using the number of people participating in polls, early voting, absentee voting, provisional voting and the eventual voter turnout (5 variables.) 

### Democrat
- Cluster 1: Fewer number of democrats participated in all polls, early voting, absentee voting, provisional voting, and the eventual turnout was much less than average.
  - Allegany, Caroline, Cecil, Dorchester, Gamett, Saint Mary’s, Washington, Wicomico, Worcester
- Cluster 2: Many more democrats participated in polls, early voting, absentee voting, provisional voting, and the eventual turnout rate is a slightly higher than average
  - Baltimore City, Baltimore County, Montgomery, Prince Georege’s
- Cluster 3: Fewer number of democrats participated in polls, early voting, absentee voting, provisional voting, but the eventual turnout was a lot higher than average
  - Anne Arundel, Calvert, Carroll, Charles, Frederick, Harford, Howard, Kent, Queen Anne’s, Somerset, Talbot
  <img width="1237" alt="Democrat" src="https://user-images.githubusercontent.com/70663111/97830416-e35d0e80-1c9a-11eb-9746-491d22b97d8c.png">
  
  ### Republican
- Cluster 1: More republicans participated in polls, many more participated in early voting, more participated in absentee voting, extremely slightly more participated in provisional voting, final turnout was higher than average
  - Carroll, Frederick, Harford, Howard, Prince George’s
- Cluster 2: Much fewer republicans participated in polls, early votings, fewer participated in absentee voting, much fewer in provisional voting, final turnout was higher than average
  - Allegany, Baltimore City, Calvert, Caroline, Cecil, Charles, Dorchester, Garrett, Kent, Queen Anne’s, Saint Mary’s, Somerset, Talbot, Washington, Wincomico, Worcester
- Cluster 3: Extremely more republicans participated in polls, early voting, absentee voting, provisional voting, final turnout was higher than average
  - Anne Arundel, Baltimore County, Montgomery

<img width="1248" alt="Republican" src="https://user-images.githubusercontent.com/70663111/97830420-e526d200-1c9a-11eb-8cb2-82cdd4d2fb68.png">

## Work with Excel
1. Clean the data: deleting unecessary data except for polls, early voting, absentee voting, provinsional voting, turnout
2. Calculate the mean and standard deviation or all variables in each state by MEAN() and STD.DEV()
3. Standardize four attributes using STANDARDIZE() for z-scores
4. Choose Allebany, Prince George;s, Washington as three anchors and use VLOOKUP() to find their z-scores
5. Calculate the distance between each z-score with the corresponding of the anchors, and use MIN() to find the minimum distance, then use MATCH() to find the anchor in which the minimum distance belongs
6. Calculate the sum of minimum distances and use solver to do cluster analysis based on different race categories


# Summary
For both Democrats and Republicans in Maryland, the counties that were very active in all categories were not the majorities. Republicans who were less active in every voting stage were much more than the number of Democrats. While being less active, the final turnout rate of these people were still higher than average. Compared with Democrats however, although Democrats in Maryland could have been active in every voting stage, the eventual turnout rate could be just moderate considering how much they have participated in the other processes. 

Interestingly, there is unlikely a corresponding pattern between activity level of Republicans and Democrats in the same county. What the clusters in both parties show is that the activity level of a county in voting steps  can reflect in both Republicans and Democrats, such as those in Baltimore County and Montgomery. Republicans and Democrats in Allegany, Caroline, Cecil, Dorchester, Garrett,  Saint Mary’s,Washington, Wincomico, Worcester are both less active in the voting process, except that Republicans still vote while democrats vote a lot less than average. 

The reasons behind these differences are yet to be determined. The only thing that can be sure is that voting is an important right of citizens. To create an atmosphere that encourages everyone to speak up and take action is important in alleviating many social problems and disagreements. Compared with other states that might witch hunt those of any supporter of a single political party, Maryland is not showing the same fault. 


  

