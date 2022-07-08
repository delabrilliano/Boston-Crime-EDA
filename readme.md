# **Exploratory Data Analysis on Crimes in Boston Dataset**
![asd](https://github.com/delabrilliano/Boston-Crime-EDA/blob/main/image/topic-boston-gettyimages-564358796-promo.jpg?raw=true)
**By: Delabrilliano Ismail**
<hr>

## **Background**
Boston, officially the City of Boston, is the capital and most populous city of the Commonwealth of Massachusetts in the United States and 24th-most populous city in the country. The city proper covers about 48.4 sq mi with a population of 675,647 in 2020, also making it the most populous city in New England.
<hr>

## **Data Understanding**
We use the data that we get from Boston Police Department website and use the database from 2015-2021. All of the data contains 17 columns that are described below:

1. **INCIDENT_NUMBER**: Unique number of each case (One case can contain multiple offences)
2. **OFFENSE_CODE**: Code of Crime's Offense.
3. **OFFENSE_CODE_GROUP**: Name of the offense.
4. **OFFENSE_DESCRIPTION**: Description of the offense.
5. **DISTRICT**: Boston Disctrict Code
6. **REPORTING_AREA**: Area number where crimes occurred.
7. **SHOOTING**: Indicate if there are a shooting involves.
8. **OCCURRED_ON_DATE**: Time of incidents/crime.
9. **YEAR**: Year of the occurred crimes.
10. **MONTH**: Month of the occurred crimes.
11. **DAY OF WEEK**: Day of the occurred crimes.
12. **HOUR**: Hour of the occurred crimes.
13. **UCR_PART**: Uniform Crime Reporting Offence types.
14. **STREET**: Street name where crime occurred.
15. **LAT**: The latitude where the crime happened.
16. **LONG**: The longitude where the crime happened.
17. **LOCATION**: Combination of Lat and Long (Lat, Long).


**Project Limitation**

1. This project will use the database that is provided by Boston Police Departement (BPD) from 2015-2021. But, the data from 2015 started only from June. So later we will drop all of the 2015 data.

2. The UCR PART columns data is only available until 2018. So later when we analyze the column, we will only analyzing the crime that occurs 2016-2018.

3. There are several Offense Code meaning that are not available on the BPS website. So later we will use the Offense Description column value for the Offense Code Group missing value.

_Database Source:_ 
 
 [Kaggle](https://www.kaggle.com/datasets/AnalyzeBoston/crimes-in-boston) | [BPD Website](https://data.boston.gov/dataset/crime-incident-reports-august-2015-to-date-source-new-system)
<hr>

## **Problem**

__Problem Statement__

1. Using the data from Federal Bureau of Investigation (FBI) and the Bureau of Justice Statistics (BJS), Pew Research Center have found that Americans tend to believe crime is up, even when the data shows it is down. In 20 of 24 Gallup surveys conducted since 1993, at least 60% of U.S. adults have said there is more crime nationally than there was the year before, despite the generally downward trend in national violent and property crime rates during most of that period.
> Source: https://www.pewresearch.org/fact-tank/2020/11/20/facts-about-crime-in-the-u-s/

2. The crime rate in Boston is considerably higher than the national average across all communities in America from the largest to the smallest, although at 26 crimes per one thousand residents, it is not among the communities with the very highest crime rate. The chance of becoming a victim of either violent or property crime in Boston is 1 in 38. Based on FBI crime data, Boston is not one of the safest communities in America. Relative to Massachusetts, Boston has a crime rate that is higher than 98% of the state's cities and towns of all sizes. 
> Source: https://www.neighborhoodscout.com/ma/boston/crime#description

To summarize, the problems that we will try to answer are:

1. Is it true that the numbers of crimes is up each year?

2. What can the government (Including the Police) do to reduce the crime numbers in Boston and make it safer for the citizen?

3. What can the citizen of Boston do to keep themselves safe?
<hr>

## **GOALS**
1. Finding the trends of crime number in general year over year.

2. Recommend an action to be taken by the government to make Boston a lot safer.

3. Giving recommendation for citizen of Boston to avoid crime in their city.
<hr>

## **EDA RESULTS**

**Insights**
1. Crime in Boston hit its peak on 2017, and have been on the downtrend afterwards, and start rising again on 2021.
2. On Monthly analysis, Crimes in Boston from 2016 - 2021, peaked in the month of August.
3. On Season analysis, crime in Boston is rising and peaked until summer and start to goes down on Autumn to Winter. And then it will start to rise again during spring until Summer.
4. June-November is the range of months that crimes most likely to occur in Boston.
5. Most of the crimes in Boston on 2016-2021 occurred after 7 am until 11 pm and suddenly spiked on 12 a.m.
6. Crimes in Boston are almost equally distributed throughout Monday-Saturday, and Sunday being the lowest day of crimes occurred, and Friday being the day for the most occurred crime.
7. There is a significant differences between number of crimes that occurred on Weekend and Weekdays, and Weekdays being the higher number of crimes that occurred.
8. Crimes in weekdays usually occurs on workhour, while crime in weekend usually occurs on non-workhour. (Workhour is 9am - 5pm)
9. The crime's offense type that occurred the most on Boston in 2016 - 2021 is Investigate Person, followed by Motor Vehicle - Leaving Scene - Property Damage, and Sick/Injured/Medical - Person
10. On the total crimes that occured on Boston, there is actually a really small portion of crimes that involved shootings (0.07%)
11. There are no significant number of shooting crime frequency except for crime's offences of 'Investigate Property'. This offence involved burglary, larceny-theft, motor vehicle theft, and arson.
> Source: https://ucr.fbi.gov/crime-in-the-u.s/2010/crime-in-the-u.s.-2010/property-crime
12. The other noticable offences that involved shooting is assault D/W (deadly weapon) on Other and Police Officer, and Ballistic Evidence/Found. All of this offences is expected to have high number because it is directly involve with gun.
13. Even though that 'Investigate Person' is the type of offences that is mostly occurred in Boston on 2016 - 2021, the offences is rarely involving a shooting, with only 107 shooting in the period of 2016-2021
14. The trend on shooting crime is different compared to trend on crime in general from 2016 to 2021. It can be seen that from 2016-2018, the changes never past 100 count, and then from 2018-2019, the number of shooting almost tripled from 319 to 810, and hit its peak on 2020 with 1.122 shooting crime.
While 2020 to 2021 the shooting number was reduced to 909, the number is still a lot higher than 2016-2018 numbers.
15. The trend for crime's offences that involves shooting is similar with crime in general. The numbers peaked on Summer and went down on Autumn and Winter,and will rise again in Spring.
16. Most of the crimes in Boston on 2016-2018 classified as UCR Part Three with the proportion of (51%) and 'Others' being the least classification with the proportion of just 0.4%.
17. Crime's offences that caused high severity (UCR Part One) is involving Larceny/Robbery, Assault, and Breaking & Entering.
18. The trends for crime that is classified as Part One on UCR, is almost the same crime in general. The only diffenrence is that the Part One crime is almost equally distributed in each season.
19. Highly severe crime mostly occurs on weekdays and outside of workhour (both on weekend and weekday)
20. There are a lot of heat (crimes occurred) on Roxbury, Dorchester, and South End districts.
21. The highly severe crime (UCR Part One) oftenly occurs on Boston's South End district. While the other district does not have higher heat like South End district.
22. Shooting oftenly occurred around Roxbury, Mattapan, and Dorchester. On the other districts, the heat are not as high as those 3 districts.
<hr>

## **Analysis and Recommendation**
**Insight Analysis**
1. Contrary to the research conducted by Pew Research, we have found that Crime in Boston actually rose from 2016-2017 and 2020-2021. However, it is true that crime number in USA generally went down year after year. This gaps between crime numbers in city and crime numbers nationally, is maybe the reason that lot of people believed that crime number is rising.

>Source: https://www.disastercenter.com/crime/uscrime.html
2. We found that crime number on Summer is the highest compared to other season. This finding is in line with the research conducted by U.S. Department of Justice, Bureau of Justice Statistics, that people are more likely to be a victim of violent crime during the summer season. And based on our findings, the UCR Part One is also having the highest occurrence on summer. 

> Source: https://bjs.ojp.gov/content/pub/pdf/ics.pdf

> https://www.thv11.com/article/news/crime/crime-increase-in-the-summer-time-yes/91-00e333f3-0cd3-4e54-8a51-5f98622f6692

3. Based on our findings, we have found that crimes in general, mostly occurs on Weekdays on work-hour, While highly offensive crime (UCR Part One) oftenly occurs outside workhour. This finding is in line with the research that was published by The Sleep Judge entitled "The Crimes at Night: Analyzing Police Incident Reports in Major Cities" where they found that violent crimes occur most often at night and police incidents tend to happen between Monday and Friday. 
> Source: https://www.thesleepjudge.com/crimes-that-happen-while-you-sleep

4. Most crime's offences in Boston are classified as medium-low severe, with most crime's offences that occured are Investigate Person, Motor Vehicle incidents, and response to sick/medical/injured person. This finding's is also in line with shooting crime proportion in Boston which is very low (0.07%). However, we should notice that there are a significant uptrend of number of shooting crime in Boston. from 2018-2019, the number of shooting almost tripled from 319 to 810, and hit its peak on 2020 with 1.122 shooting crime. While 2020 to 2021 the shooting number was reduced to 909, the number is still a lot higher than 2016-2018 numbers.
From the analysis we know that shooting crimes oftenly occured on burglary, larceny-theft, motor vehicle theft, and arson offence. The rising numbers of shooting on 2019 to 2020 is well may be caused by those crimes related to COVID-19 pandemic. Based on the research conducted by ```Matthew P. J. Ashby entitled "Initial evidence on the relationship between the coronavirus pandemic and crime in the United States"```, the research have found that public health crises affect crime rates. The chief of media relations for the Boston Police Department, Sgt. Detective John Boyle, has said that due to the widespread unemployment brought upon many people by the pandemic, Boston Police expected property crimes such as breaking-and-entering, theft, robbery. In which, those crimes are oftenly include shooting. 
> Source: Ashby, Matthew PJ. "Initial evidence on the relationship between the coronavirus pandemic and crime in the United States." Crime Science 9.1 (2020): 1-16

> https://thesuffolkjournal.com/36697/news/the-covid-19-pandemic-and-its-effect-on-bostons-crime-rate/

5. From the data analysis, we can conclude that Roxbury, Dorchester, Mattapan, and South End is the districts where most crime occurred.

**Recommendation**

1. We can conclude that even though the crime rate is down nation-wide, but crime rate in Boston specifically is actually fluctuate over the year. To make the public feel safer, especially the locals/residents, one of the initiatives the government can take is NeighborhoodStat. NeighborhoodStat was envisioned by the New York City Mayor’s Office of Criminal Justice (MOCJ) as a strategy for bringing residents together with city leadership to jointly address persistent challenges within the city’s public housing developments. NeighborhoodStat empowers residents to set their own agenda for addressing the issues affecting the safety of their neighborhoods and puts in place a structure allowing them to partner with city leaders to bring their vision into reality.

    New York’s approach has proved effective. When MAP was founded in 2014, the target communities accounted for nearly 20 percent of violent crime across the city’s 328 public housing developments. Since then, crime and violence have fallen significantly. Target communities have experienced an 11 percent reduction in violent crime and a 10 percent reduction in the major crime categories known as index crimes. And while crime rates have been trending downward across the city of New York, target developments have outpaced other New York City Housing Authority developments in crime reduction.
> Source: https://www.americanprogress.org/article/neighborhoodstat-strengthening-public-safety-community-empowerment/
2. a. From a research entitled ```"Summer jobs reduce violence among disadvantaged youth." (Sara B. Heller, 2015)```, it is founded that Summer Jobs can lower the crime rate during summer, especially on teenager. The researcher have found 43% reduction in arrest for violent crimes among youths.

- Government: Based on that research, the government can give an extra incentive to the youth or family member that are willing to take the summer jobs program.

- Citizen/Residents: Citizen/Residents can encourage their relatives/family member to take the summer jobs program

> Source: Heller, Sara B. "Summer jobs reduce violence among disadvantaged youth." Science 346.6214 (2014): 1219-1223.
2. b. Other initiatives that the government can take is the "Summer Crime Prevention Initiative" that is being run by DC Government since 2010. The initiative will focuses the Boston Police Department (BPD) to deploy all available resources and calls upon partner agencies and organizations to assist in a coordinated effort to eliminate violent crime in the disctrict that have high-density of crime.
> Source: https://mpdc.dc.gov/page/summer-crime-prevention-initiative
3. Other than the NeighborhoodStat initiatives, the government (including the police) and the residents of Boston can take an initiatives such as reducing alcohol availability, improving street connectivity, and providing green housing environments that is proven can reduce violent crimes (UCR Part One).

    Also, the government and residents of Boston can make a regulation of curfew that is customized for each districts or neighborhood.
> Source: Kondo, Michelle C., et al. "Neighborhood interventions to reduce violence." Annual review of public health 39.1 (2018): 253-271.
4. Based on the research conducted by ```Sanchez, Carol, et al. entitled "A systematic review of the causes and prevention strategies in reducing gun violence in the United States." on 2020```, the researchers have found that Gun violence is pervasive and multi-factorial. Interventions aimed at reducing gun violence should be targeted towards the most common risk factors cited in the literature such as access, violent behavioral tendencies due to past exposure or substance abuse, and mental illness including suicidal ideation.

    Related to that findings, the action that can be taken by the governments are:

- Reduce easy access to dangerous weapons. e.g: Mandatory background check for people who want to buy a gun
- Support gun violence research. e.g: Ensure that the Centers for Disease Control and Prevention (CDC) and others have the resources to study this issue and provide science-based guidance. 
- Hold the gun industry accountable and ensure there is adequate oversight over the marketing and sales of guns and ammunition.

    Other policies that can be taken by the governments are limiting children's access to guns, restricting concealed-carry permits, and restricting "stand your ground" policies. Based on the research conducted by Michael Price on 2020, these 3 policies can reduce gun deaths by more than 10%.
> Source: https://www.preventioninstitute.org/focus-areas/preventing-violence-and-reducing-injury/preventing-violence-advocacy

> Source: https://www.science.org/content/article/three-types-laws-could-reduce-gun-deaths-more-10)

5. The government and the citizen of the hot-spot district can work together to implement an action that can help to reduce crime such as:
-  Improvements to the public realm—such as urban greening and tree canopy programs in urban neighborhoods. 

> Source: Kondo MC, South  EC, Branas  CC, Richmond  TS, Wiebe  DJ.  The association between urban tree cover and gun assault: a case-control and case-crossover study.
- Increasing the number of spaces for informal contact between neighbors. 

> Source: Sullivan, W. C., Kuo, F. E., & Depooter, S. F. (2004). The fruit of urban nature: Vital neighborhood spaces. Environment and behavior, 36(5), 678-700
- Create a Community-Based and Civic Organizations in leading anti-violence programs. 

> Source: Sharkey, P. (2018). Uneasy peace: The great crime decline, the renewal of city life, and the next war on violence. WW Norton & Company.
<hr>


_**Get in Touch:**_

| [Linkedin](https://www.linkedin.com/in/delabrilliano-ismail-05758715a/) | [Github](https://github.com/delabrilliano) | [Tableau](https://public.tableau.com/app/profile/delabrilliano.ismail)
<hr>