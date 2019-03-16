# languages-and-population
Of the more than 6,900 languages spoken worldwide, 10 languages are the mother tongue of half the world's population. The majority of the world's population also speak a second language. The paper first presents some background and then makes appropriate assumptions to model the to simplify the model. Papers will build a regression model of language, which is divided into the first language and the second language modeling. In the first language modeling, the growth coefficient of each language is calculated according to the influence of Malthusian Population Model and global population migration. In the second language modeling,we mainly study the factors that affect the usage of each language, including political, economic, military, cultural and other aspects of influence, and we have chosen three parameters to quantify this influence. The three parameters are calculated for each language Parameter value. According to the modeling results, we predict the population of each language in the next 10 years and 50 years and plot the population over time with MATLAB.We then select the top six languages, and according to the regional economic development situation we choose the address of a multinational branch, butthe suggestion made by us can be different between the next 10 years and the next 50 years. We then summarize the factors impactingon language usage and changes in users and geographic distribution. Finally, we analyze and summarize the advantages and disadvantages of the model and draw conclusions.

________________________________________2018MCM/ICM Summary Sheet
Summary
Of the more than 6,900 languages spoken worldwide, 10 languages are the mother tongue of half the world's population. The majority of the world's population also speak a second language. The paper first presents some background and then makes appropriate assumptions to model the to simplify the model.
Papers will build a regression model of language, which is divided into the first language and the second language modeling. In the first language modeling, the growth coefficient of each language is calculated according to the influence of Malthusian Population Model and global population migration. In the second language modeling,we mainly study the factors that affect the usage of each language, including political, economic, military, cultural and other aspects of influence, and we have chosen three parameters to quantify this influence. The three parameters are calculated for each language Parameter value.
According to the modeling results, we predict the population of each language in the next 10 years and 50 years and plot the population over time with MATLAB.We then select the top six languages, and according to the regional economic development situation we choose the address of a multinational branch, butthe suggestion made by us can be different between the next 10 years and the next 50 years. We then summarize the factors impactingon language usage and changes in users and geographic distribution.
Finally, we analyze and summarize the advantages and disadvantages of the model and draw conclusions.
Keywords: population growth; language; economy

 
Contents
1	Introduction	2
1.1 Problem Background	2
1.2 Our Work	2
2	Assumptions	2
3	Nomenclature	3
4	Statement of our Model	3
4.1 Modeling of L1	4
4.1.1	 Modeling of P1	4
4.1.2	 Modeling of S	6
4.2	Modeling of L1	6
4.2.1	 The overall strength of language i：enc(i)	7
4.2.2	 The Language's Influence As The world's Academic Communication Language: aca(i)	8
4.2.3 The importance of the language as a foreign language in the rest of the world: edu(i)	8
4.3	 The Analysis of The Model	9
4.4	 The Model Results	11
4.4.1 Influencing Factors and Predictions	11
4.4.2 Advice on New International Office selection	12
5	Strengths and Weaknesses	13
5.1	Strengths	13
5.2	Weaknesses	13
6	Conclusions and Further Discussion	13
7	Brief Memo to The Chief Operating Officer	14
References	15
Appendices	16
Appendix A  Code Used to Fitting Curves in MATLAB	16
Appendix B  Code Used to Predicted Language Usage	18


 
1	Introduction
The development of language in the context of globalization is a topic of common concern and is closely linked to the life of every individual. Whether it is studying abroad, immigration, or the construction of multinational corporations, what we can’t deny is that language is an important factor that all of us need to consider. The article analyzes the trends and influencing factors of ten linguistic population changes, and establishes a mathematical model to answer the questions concerning the branch-building of transnational corporations that are asked in the title.
1.1 Problem Background
Language is a tool for people to witheachother. In more than 6,900 languages worldwide, the sum of the number of users in 10 languages reaches half of the world's population. The number of speakers of language varies depending on a number of factors, such as economic, political, educational, immigration and so many other factors. With the progress of globalization and the development of high-tech means of communication such as the Internet, language learning is more convenient and study abroad becomes the choice of more and more people. Nowadays, we can see many more people can learn the second languages and even the third languages, and the language usage population is changing complexly and diversely but the research on it is exciting and wonderful.
1.2 Our Work
After careful reading of the subject, appropriate arrangements have been made for our task.
In this paper, we have collected data on the number of users in ten languages provided in previous years and used it to establish a regression model. By using time as abscissa and population as ordinate, a linear regression equation is fitted by using software to predict the number of language users in the next few years. We mainly consider the future population of the language and the country's overall strength to determine the location and language of the branch.
Short-term and long-term recommendations are not the same exactly. For the consideration of 50 years later, we will carry out a qualitative analysis based on the trend of studying abroad and immigration around the world. The result of consideration after 50 years and the result of consideration after 10 years will be different.
In Section.2,we create some assumptions to simplify the problem.In Section.3 … Section.4 … Section.5, we analyze the advantages and disadvantages of the model.
2	Assumptions
In the dissertation, we make some assumptions to simplify the problem and therefore facilitate analysis and calculation.
	We assume that no war will occur in the next 50 years because no country has ever been willing to bear the extremely enormous cost of the war in the peace era and the factors influencing the number of people who use it in various languages have nothing to do with the war.
	We ignore the restrictions on land resources when modeling.
	We temporarily assume that the world economy is in stable development without any economic crisis.
3	Nomenclature
In this paper, we use the nomenclature in Table 1 to describe our model.
Table 1: Nomenclature
Symbol	Deﬁnition / Description
i	the ith languagewe will study
t	time (t years later)
L1	the first language
P1 (i, t)	the number of people in the area where language i is the native language after t year(s)
S (i, t)	the number of population movements using language i after t year(s)
L2	the second language
P2	the number of L2 in 2017
enc (i)	the influence of language, which is associated with the use of the language as a native speaker of the area of national power
aca (i)	the influence of a language when the language is as the academic exchanges in the world
edu (i)	the importance of a language in other parts of the world as a foreign language to learn

4	Statement of our Model
The language usage model is divided into two parts, the first language (L1) and the second language (L2). Based on the number of L1s and the number of people in the region using the language, the Malthusian Population Model [2] is used to model this model. In addition, considering the influence of the world's population migration on L1, the existing model is further optimized. The change of L2 quantity is closely related to the language's own influence. The modeling mainly considers the impact of the language-speaking areas on the world in terms of politics, economy, culture, military, science and technology. In the past years, the average of the L2 data of the language is the basic data, and the L2 is corrected according to the three main parameters (education: edu), (academic: aca), and (economic: eco) that are set for each language. For the next 50 years, most languages will maintain their existing areas of use, but there are also special cases where the geographical distribution will be extended over time.
According to the model in the previous section, we get the top six languages integrated, and we chose six more desirable international office addresses depending on the level of economic development in the regions where these languages are used. In the short term (10 years), Beijing, London, Saudi Arabia, Madrid, Moscow and Chittagong are advised while in the long run (50 years), London, Beijing, Saudi Arabia, Madrid, Bangalore and Chittagong are suggested.
We let L denote the total number of people who use a certain language; L1 represents the number of native speakers in the language and L2 represents the number of people who use the language as a second language. We use different approaches to L1 and L2 modeling.
4.1 Modeling of L1
L1 is related to the number of people and mainly includes two factors: the change of population over time and the factors of population migration, which can be expressed as the following formula (1):
L1(i,t)=P1(i,t)+S(i,t)                              (1)
where:
	i represents the language;
	t means time (t years later);
	P1 (i, t) is the number of people in the area where language i is the native language after t year(s);
	S (i, t) represents the number of population movements using language i after t year(s)
4.1.1	Modeling of P1
P1 is modeled by the Malthusian population model, that is:
P1(i,t)=P(i,0)e^(r_i∙t)                                    (2)
Since the political, economic and social stability factors determine that the coefficient of population growth in each region is different, ri said that the growth coefficient of language i. The determination of ri for each language i is derived from the data in the following table[1], where the data units are in million:
Table 2: Number of Language Users in Certain Years
Order	ithLanguage	2017	2007	2010	1999
1	Mandarin	897	935	955	937
2	Spanish	436	390	405	332
3	English	371	365	360	322
4	Hindi	329	295	310	182
5	Arabic	290	280	295	175
6	Portuguese	218	205	215	170
7	Bengali	242	200	205	189
8	Russian	153	160	155	170
9	Japanese	128	125	125	125
10	Punjabi	148	95	100	
11	German	76	92	95	98
12	French	76	75		80
13	Malay	77	77		
The value of ri after modeling is as the following table:
Table 3: The Growth Coefficient of Each Language
Order	ithLanguage	ri
1	Mandarin	0.00705494
2	Spanish	0.0125801
3	English	-0.00459777
4	Hindi	0.0165323
5	Arabic	0.0173953
6	Portuguese	0.015876
7	Bengali	0.00823087
8	Russian	-0.0105829
9	Japanese	0
10	Punjabi	0.0170978
11	German	0.0106961
12	French	
13	Malay	

4.1.2	Modeling of S
S (i, t) is determined by the data obtained from the investigation. According to the data, the number of migrants is not too high, accounting for about 3.3% of the total population each year. There are 47 million people who have emigrated to the United States, ranking Germany, Russia and Saudi Arabia at the top. Britain and Canada each received about 8 million immigrants; the most populous country was India, a total of 16 million immigrants; followed by 12 million in Mexico and 11 million in Russia; the fourth is China, 1000 Million people.
Thus, S (i) has a positive change in the number of English, German and French, while Chinese and Hindi have a negative change.
4.2	Modeling of L1
Firstly, for the numerical modeling of L2, the average value of L2 of each language was used as the base number P2. Since the world began to register the second language in the census, it began in recent years, and its data is limited. The data in 2017 is the standard base. Then, we mainly consider: (1) the influence of language, which is associated with the use of the language as a native speaker of the area of national power (represented as enc), (2) the influence of a language when the language is as the academic exchanges in the world (represented as aca), (3) the importance of a language in other parts of the world as a foreign language to learn (represented as edu). The relationship between the three factors and the L2 can be expressed as the formula (3):
L2(i,t)  =P2(i)  * e^(（enc(i)+aca(i)+edu(i) ）  * t)            (3)
where:
	i represents the language;
	P2 can be seen in the following table of values for the value of P2 (i) (that is, the number of L2 in 2017) 
Table 4: The Value of P2 and Its Rank of Each Language
Order	ith language	P2(i)	Rank
1	Mandarin	193 million	4
2	Spanish	91 million	8
3	English	611 million	1
4	Hindi	215 million	2
5	Arabic	132 million	6
6	Portuguese	11 million	15
7	Bengali	19 million	13
8	Russian	113 million	7
9	Japanese	1 million	19
10	Punjabi		
11	German	52 million	12
12	French	153 million	5
13	Malay	204 million	3
Here are the design of three parameters: enc (i), aca (i), edu (i):
4.2.1	The overall strength of language i：enc(i)
According to the linguist George Weber's research, what kind of rank and position a language has in today's world depends on six indicators:
	Use the language as a native speaker (4 points)
	Use this language as a non-native speaker (6 points)
	Number and population of countries using the language (7 points)
	Economic, scientific and technical strength of the country where the language is used (8 points)
	Frequency of use of the language in the fields of diplomacy, international trade, academic exchange, etc. (8 points)
	Reputation in Social and Humanities (4)
Additionally, if it is the official language of the United Nations, we can add 3 points. The perfect score is 40 points.
Theses six indicators can be accepted as the judgment of a language in today's world ranking and we regard them as comprehensive indicators of status. Correspondingly determine the value of enc, as the following table:
Table 5: The Value of enc(i) and Its Score of Each Language
Order	ith language	Score	enc(i)
1	English	37	0.033*0.25
2	French	23	0.033*0.13
3	Spanish	20	0.033*0.1
4	Russian	16	0.033*0.06
5	Arabic	14	0.033*0.04
6	Mandarin	13	0.033*0.04
7	German	12	0.033*0.02
8	Japanese	10	0.033*0.01
9	Portuguese	10	0.033*0.01
10	Hindi	9	0
4.2.2	 The Language's Influence As The world's Academic Communication Language: aca(i)
Table 6:The Value of aca(i) of Each Language
Order	ith language	aca(i)
1	Mandarin	0.001
2	Spanish	0.003
3	English	0.005
4	Hindi	0
5	Arabic	0
6	Portuguese	0.001
7	Bengali	0
8	Russian	0.002
9	Japanese	0.001
10	Punjabi	0
11	German	0.001
12	French	0.001
13	Malay	0
4.2.3 The importance of the language as a foreign language in the rest of the world: edu(i)
Table 7:The Value of edu(i) of Each Language
Order	ith language	edu(i)
1	Mandarin	0.0015
2	Spanish	0.001
3	English	0.005
4	Hindi	0
5	Arabic	0.001
6	Portuguese	0
7	Bengali	0
8	Russian	0.001
9	Japanese	0
10	Punjabi	0
11	German	0.0005
12	French	0.0005
13	Malay	0
4.3	The Analysis of The Model
Therefore, combining of formulas (1), (2), (3), we can conclude that L is calculated as:
L(i,t)=P(i,0) e^(ri∙t)+ S(i,t)+ P2(i)* e^(（enc(i)+aca(i)+edu(i)）t)     (4)
We use MATLAB software to draw the curve of changes in language use of the population:
 
Figure 1:Languages by Total Numbers of Speakers
And the code can be seen in Appendix A and Appendix B.According to the formula, the total number of users in each language after 10 years and 50 years is calculated as the following table:
Table 8:The Total Number and Rank of Usersin Each Language After 10 and 50 Years
Order	ith language	Total Number in 2017 (million)	Total Number After 10 Years（million）	Rank	
After 10 Years	Total Number After 50 Years（million）	Rank	
After 50 Years
1	Mandarin	1090	1163 	1　	1510 	2
2	English	983	1088 	2　	1817 	1
3	Hindi	544	603 	3　	967 	3
4	Spanish	527	592 	4　	949 	4
5	Arabic	422	480 	5　	840 	5
6	Malay	281	283 	6　	291 	9
7	Russian	267	256 	9　	235 	11
8	Bengali	261	282 	7　	384 	7
9	Portuguese	229	267 	8　	494 	6
10	French	229	238 	10　	280 	10
11	Punjabi	148	176 	11　	348 	8
12	Japanese	129	129 	13　	129 	13
13	German	129	138 	12　	188 	12
In the table above, the change in language rankings validates the following facts: (1) the rise in English language proves that English is and will be the most powerful language in the world today; (2) decline in Chinese rankings stems from the fact that Chinese people have a high immigration rate, and some people have been assimilated after immigrating and abandon Chinese, while other countries have fewer learners of Chinese and most Chinese-speaking regions have not received it; (3) the decline in the number of Russians stems, which is from the stagnation of population growth in the Russian region on the one hand and is from the decline of Russia's global influence on the other hand; (4) the number of Portuguese speakers language will increase in number.
These data provide a good illustration of the current language use in society and are largely influenced by the government's efforts to promote education, social pressures, migration and assimilation of cultural groups in schools and other languages spoken by immigrants. In addition, In the era of globalization and the Internet, language-influencing factors also include international business relations, growing global travel, the use of electronic communications and social media.
4.4	 The Model Results
4.4.1 Influencing Factors and Predictions
Under the influence of time and the process of globalization, there has been a steady increase in the number of language users with a certain number of bases (> = 5000000). The increase is partly due to the natural increase of population in the area where the language is spoken. This is the most basic and important factor in the development of language. The other part comes from immigrants in other languages. A tremendous impact of this trend is the reduction of linguistic diversity. Some minorities now face the endangered situation will be more serious. However, due to the concentration of mainstream languages, world commerce and trade activities are easier to expand, which plays a role in promoting the world economy. 
In our view, the basic language development lies in the number of first language users, and population growth is the factor that determines the number of first language users. Therefore, if a country's population growth stagnates or even increases in the opposite direction, the number of users of the language in the future may also experience a reverse growth. In our analysis, India, as a developing country, has made a steady increase in the number of Indians using its vast population base and a growing demographic model. In contrast, Japan and the world's third-largest economy, despite their huge economic volume and overseas competitiveness, have also stagnated in the number of Japanese users in a period of stagnation in their population growth
There are two major trends in the world population migration pattern. One is the concentration of population on the coastline and the other is the concentration of population on cities. As mentioned earlier, languages with a certain number of foundations are more conducive to attracting other populations, and attracted populations tend to be concentrated in large and medium-sized cities in the language use areas.
4.4.2 Advice on New International Office selection
According to George Weber's research, indicators are now being revised to better reflect the economic proficiency score of the language. Scoring reference standards are as follows:
	the number of people using the language as a first language; (10 points)
	the number of people using the language as a second language; (15 marks)
	the total population and the number of countries using the language; (10 points)
	the use of the language of the region's economic development; (20 points)
	Potential capital in the area where the language is spoken; (20 points)
	the use of the language of the region's attitude toward foreign capital; (10 points)
	the use of the language of the region can compete for market share; (10 points)
	if it is the United Nations official language,plus5 points.
The total score of 100 points.
We determine the score for each language, as shown in the following table:
Table 9:Language Scoreand Rank
Order	Language	Score（10years later）	Rank	Score（50years later）	Rank
1	Mandarin	97	1	96	2
2	English	95	2	98	1
3	Hindi	80	8	83	5
4	Spanish	85	4	85	4
5	Arabic	90	3	90	3
6	Malay	75	10	73	11
7	Russian	85	4	80	8
8	Bengali	83	6	83	5
9	Portuguese	81	7	81	7
10	French	79	9	79	10
11	Punjabi	75	10	80	8
12	Japanese	68	12	68	13
13	German	70	11	70	12
To sum up, in the short term (10 years), our proposal is to start a new branch in turn in Beijing, London, Saudi Arabia, Madrid, Moscow and Chittagong. However, in the long run (50 years), our advice is different. In order of priority, they are London, Beijing, Saudi Arabia, Madrid, Bangalore and Chittagong respectively.
5	Strengths and Weaknesses
5.1	Strengths
	Data are withhigh credibility because we select them from reliable official website.
	When using the software for fitting, the formula of curve fitting is more accurate and the fitting degree is better, which is helpful to the population model prediction.
	We have effectively quantified the problem so that the problem is translated into a mathematical problem.
5.2	Weaknesses
	For some years, we did not find the corresponding data, and when fitting we ignore the part of the data that is not found, which has some negative effects on the forecast.
	For the analysis of the long-term linguistic population distribution model, we have only conducted qualitative analysis because of the difficulty of finding data and not yet carrying out quantitative analysis.
	The model made by us is lacking of reliability and sensitivity verification.
6	Conclusions and Further Discussion
With a certain background and appropriate assumptions, a regression model is established. We model the first language and the second language separately and combine the formulas from the two parts. Using the formula, we predict the changing trend of language usage, we conclude that the number of people who use language will rise and English will become the most powerful language.The number of users in Portuguese will also rise, while the number of users in Chineseand Russian use will decline.
There is a steady increase in the number of users with a certain number of bases (> = 5000000), but the diversity of languages will be reduced. Some of the minorities will be endangered, but language barriers to international trade exchanges will be reduced, which tend to promote the international economy.
We predict and rank the number of people who use language based on the model we have got and find that some languages will be replaced. For example, Russian ranked ninth in 10 years but ranked eleventh in 50 years and Punjabi in 10 will rank eleventh year but will rank eighth after 50 years.After analyzing and forecasting, we think that population concentration in the coastline and in the cities can be the two major trends in the world population migration pattern and therefore the distribution of languages will then be concentrated in coastal and urban areas.
The data we collected was reliable, but some of the data have not been collected, whichcan affect the model building.The model did not conduct reliability and sensitivity analysis, which to some extent will have some impact on the results. However, in the process of data prediction, with the help of the reliable software and reliable formulas, the conclusions drawn by us are scientific.
7	Brief Memo to The Chief Operating Officer
According to George Weber's research, we have got the scores and therank of 13 languages in ten years and fifty years later. The short-term (ten years) proposal is to build Beijing, London, Saudi Arabia, Madrid, Moscow, Chittagong branch successively, and the long-term (ten years) proposal is to build the branches in London, Beijing, Saudi Arabia, Madrid, Bangalore, Chittagong successively.
However, as the parent company has offices in Shanghai, China, and the population using Mandarin Chinese is mainly located in eastern China.Since both Beijing and Shanghai can use Mandarin, the office in Shanghai can replace Beijing Branch. Therefore, in order to save money and human resources as much as possible, the suggestion of building a branch in Beijing can be ignored, and thusit is feasible to build less than six branches.
In addition, a lot of extra information are also in need. Firstly, we need to know the customer's local etiquette because we often encounter misunderstandings due to cultural barriers such as bowing or shaking hands before communicating with our clients. If we make a mistake, we will be misunderstood each other.Additionally, we also need to understand the local habits, because we can use life habits to predict the needs of our customers, making it easier to produce products that customers like to buy.Last but not least, we also need to understand local policies so as to avoid contradictions and conflicts with the local regulatory agencies when setting up companies, otherwise unnecessary losses will result.
References
	“List of Languages by Total Numbers of Speakers”. https://en.wikipedia.org/wiki/List_of_languages_by_total_number_of_speakers on January 17, 2018
	Frank R. Giordano, William P. Fox, Steven B. Horton. “A Frist Course in Mathematical Modeling (Fifth Edition)”[M]. China Machine Press, 2017.5: 334.



Appendices
Appendix A  Code Used to Fitting Curves in MATLAB
//Code（matlab）
x = 2010:0.1:2072;
y1 = 897*exp(0.00705494*(x-2017))+193*exp(0.00382*(x-2017));
y2 = 371*exp(-0.00459777*(x-2017))+611*exp(0.01825*(x-2017));
y3 = 329*exp(0.0165323*(x-2017))+215*exp(0*(x-2017));
y4 = 436*exp(0.0125801*(x-2017))+91*exp(0.0073*(x-2017));         
y5 = 290*exp(0.0173953*(x-2017))+132*exp(0.00232*(x-2017));             
y6 = 77*exp(0*(x-2017))+204*exp(0.001*(x-2017));
y7 = 153*exp(-0.0105829*(x-2017))+113*exp(0.00498*(x-2017));
y8 = 242*exp(0.00823087*(x-2017))+19*exp(0*(x-2017));
y9 = 218*exp(0.015876*(x-2017))+11*exp(0.00133*(x-2017));
y10 = 76*exp(0*(x-2017))+153*exp(0.00579*(x-2017));
y11 = 148*exp(0.0170978*(x-2017))+0*exp(0*(x-2017));
y12 = 128*exp(0*(x-2017))+1*exp(0.00133*(x-2017)) ;        
y13 = 76*exp(0.0106961*(x-2017))+52*exp(0.00216*(x-2017));

plot(x,y1,'Color',[1 0 0]);
hold on;
plot(x,y2,'Color',[0 1 0]);
hold on;
plot(x,y3,'Color',[0 0 1]);
hold on;
plot(x,y4,'Color',[0.5 1 0]);
hold on;
plot(x,y5,'Color',[0 1 1]);
hold on;
plot(x,y6,'Color',[1 0 1]);
hold on;
plot(x,y7,'Color',[0 0 0]);
hold on;    
plot(x,y8,'Color',[1 0.5 0]);
hold on;
plot(x,y9,'Color',[1 0 0]);
hold on;
plot(x,y10,'Color',[0 1 0]);
hold on;
plot(x,y11,'Color',[1 0 0.5]);
hold on;
plot(x,y12,'Color',[1 0 1]);
hold on;
plot(x,y13,'Color',[0 0 1]);

grid on;
legend('Mandarin','English','Hindi','Spanish','Arabic','Mylay','Russian','Bengali','Portuguese','French','Punjabi','Japanese','German');
title('Figure of Languages by Total Numbers of Speakers')


Appendix B  Code Used to Predicted Language Usage
Code (c++)
/*
* Using the established model, we calculate the total number of languages currently used in 13 languages after 10 years and 50 years*/
#include <iostream>
#include <math.h>
using namespace std;

int main()
{
int i;
double r1[13];
double p[13][3] = {
    {897,935,955},
    {436,390,405},
    {371,365,360},
    {329,295,310},
    {290,280,295},
    {218,205,215},
    {242,200,205},
    {153,160,155},
    {128,125,125},
    {148,95,100},
    {76,92,95},
    {76,76,76},
    {77,77,77}
    };

// The initial data of second language
    double p2[13] = {193,91,611,215,132,11,19,113,1,0,52,153,204};  
double r2[13] = {0.00382,0.0073,0.01825,0,0.00232,0.00133,
0,0.00498,0.00133,0,0.00216,0.00579,0.001}; // Rate of change  of second language
    double p10[13] = {}; // Data of first language after 10 years 
    double p50[13] = {};// Data of first language after 50 years
double L2_10[13]={};
double L2_50[13] = {};
double L10[13]={};
double L50[13] = {};
for(i = 0;i<13;i++){
r1[i] = (log(p[i][2])-log(p[i][1]))/3;
p10[i] = p[i][0] * exp(r1[i]*10) ;
p50[i] = p[i][0] * exp(r1[i]*50);

        L2_10[i] = p2[i] * exp(r2[i]*10);//10年
        L2_50[i] = p2[i] * exp(r2[i]*50);//50年

L10[i] = p10[i] + L2_10[i];
L50[i] = p50[i] + L2_50[i];

cout<<L10[i]<<"\t\t"<<L50[i]<<"\t\t"<<endl;
    }
return 0;
}





