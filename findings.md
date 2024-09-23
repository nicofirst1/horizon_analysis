

# Aim 
show that many ai related projects are similar and could be merged saving budget

# Start
Dowloaded projects from https://data.europa.eu/data/datasets/cordis-eu-research-projects-under-horizon-europe-2021-2027?locale=en


There are a total of 13674 projects in the file.

first step is to take only the projects with ai since we are interested in these. 
By googling i found this list with ai buzz words https://www.telusdigital.com/insights/ai-data/article/50-beginner-ai-terms-you-should-know 

after some iteration of removing words that are too specific and counting what where left i was left with these list of words with their presence in either the project objective or title

There are 2065 projects with AI in the file.


The most present ai buzz words are:
machine learning: 726
artificial intelligence : 373
ai: 309
data analysis: 118
neural network: 118
deep learning: 86
robotics: 84
big data: 72
robot: 27
natural language processing: 25
computer vision: 23
reinforcement learning: 18
data governance: 16
pattern recognition: 6
intelligent control: 6
object recognition: 6
autonomous car: 5
computational linguistics: 5
supercomputer: 5
image recognition: 5
expert system: 4
supervised learning: 4
autonomous robots: 3
speech recognition: 3
predictive modeling: 2
swarm intelligence: 2
emotion recognition: 2
decision theory: 1
evolutionary algorithms: 1
nlp: 1
bayesian network: 1
automated reasoning: 1
machine perception: 1
genetic algorithms: 1
probabilistic reasoning: 1
intelligent agent: 1
llms: 1
hidden markov model: 1
markov decision process: 1


Before moving to our aim , i wanted to investigate a bit about these projects. 
## Time
First i focused on the time, specifically the projects come with a start and end date which allows to investigate their duration.

The average duration of the projects is 41 months with a standard deviation of 14.0 months
The minimum duration is 6 months and the maximum is 85 months

specifically they are divided as such 
The number of projects in each cluster is:
0 years: 42
1 years: 274
2 years: 388
3 years: 453
4 years: 420
5 years: 467
6 years: 20
7 years: 1
most of them are below 5 years with some exceptions. This shows how 50 percentile falls below 3 years and 70 percentiles below 4 years. this is in line with the sentiment that these projects are too short making them hard to start and finish with meaningfull resutls. 



The number of projects starting each year is:
In 2021 there are 3 projects with an average duration: 40.0 months and a std of 15.0 months
In 2022 there are 483 projects with an average duration: 40.0 months and a std of 13.0 months
In 2023 there are 801 projects with an average duration: 40.0 months and a std of 15.0 months
In 2024 there are 691 projects with an average duration: 42.0 months and a std of 14.0 months
In 2025 there are 87 projects with an average duration: 36.0 months and a std of 15.0 months

the latest being 2025, which is next year


The number of projects ending each year is:
In 2022 there are 2 projects with an average duration: 6.0 months and a std of 0.0 months
In 2023 there are 28 projects with an average duration: 13.0 months and a std of 5.0 months
In 2024 there are 171 projects with an average duration: 20.0 months and a std of 6.0 months
In 2025 there are 416 projects with an average duration: 30.0 months and a std of 6.0 months
In 2026 there are 525 projects with an average duration: 36.0 months and a std of 9.0 months
In 2027 there are 459 projects with an average duration: 47.0 months and a std of 11.0 months
In 2028 there are 315 projects with an average duration: 56.0 months and a std of 6.0 months
In 2029 there are 138 projects with an average duration: 61.0 months and a std of 5.0 months
In 2030 there are 11 projects with an average duration: 67.0 months and a std of 6.0 months

it is intereting to see how the last project will finish 10 years after the start of the horizon project. given the pace of ai i think those projects proposals will probably be outdated. moreover more than half the projects will be over after 2026 (in 1 and a half year), what is the eu going to do? another horizon fund? 

From the violin plot we can see a clear (and obvius) orrelation between end date and duration






## Budget
now that we are more aware of the time analsys, let's see the budget
first we see that there are  746 projects with a budget of 0

by looking online i found out that some projects which are still in the draft phase do not report the 'totalCost' yet, so, for our estimation we need to use the  ecMaxContribution

The average non zero budget of the projects is 3161809.57 with a standard deviation of 3400367.33 (107.5% of the average): super high std! 


The minimum budget is 75000.00 and the maximum budget is 46225689.31
Let's divide the budget in cluster of millions
There are 24 budget clusters.
The number of projects in each cluster is:
0M: 554
1M: 383
2M: 392
3M: 157
4M: 166
5M: 125
6M: 67
7M: 59
8M: 54
9M: 33
10M: 18
11M: 16
12M: 4
13M: 10
14M: 8
15M: 2
16M: 1
17M: 6
19M: 2
22M: 2
23M: 1
24M: 2
25M: 2
46M: 1

we can see how most of the projects fall below 3M (70 percentile) and 90 percentile fall below 7M which is not much... 

Let's see if there is a correlation between budget and duration that we would exepct
The correlation between duration and budget is 0.31 with a pvalue of 0.0000000

well there is a slight positive correlation, but not as much as i would have expected. 

## Budget Time
so let's see how much a project has on average per month.

The average budget per month of the projects is 73578.25 with a standard deviation of 79428.91 (108.0% of the average)

The minimum budget per month is 2835.62 and the maximum budget per month is 950627.63
as previously seen, there is a lot of variation between the projects. 

The correlation between budget per month and duration is 0.31 with a pvalue of 0.0000000, budget only depends in part on the duration
The correlation between budget and start year is -0.11 with a pvalue of 0.0000002, interestingly the earlier projects seems to have less funding, or it can just be bc the earlier one last less
The correlation between budget and end year is 0.15 with a pvalue of 0.0000000


## Words
Now time to do some bag of words analysis, 
first i cleaned the objectives and titles from stowords, puctuation  then i lemmatized and remove verbs to get an idea of the most common used words
The most common words in objectives are:
data: 3071
project: 1999
system: 1835
The most common words in titles are:
system: 144
data: 142
intelligence: 136
The most common words in objectives and titles are:
data: 3213
project: 2007
system: 1979

seems like data is one of the top word everywhere , the only difference between titles and objective is intelligence in the title
the word could also emphasizes this. 

If we keep the verbs we get 
The most common words in objectives are:
data: 3447
ai: 2366
project: 2251
The most common words in titles are:
ai: 234
learning: 200
data: 174
The most common words in objectives and titles are:
data: 3621
ai: 2600
project: 2259

apparently ai was accounted as a verb...

### Words and Budget

now let's see if any words correlate with the budget, it would be interesting to see if some of the description get more moeny

Top 10 Positive Words Impacting Budget
rail           1.377523e+06
repurposing    1.289610e+06
echo           9.584387e+05
asset          9.255005e+05
hi             9.183318e+05
assets         8.015227e+05
glaciation     7.502014e+05
wafer          7.447746e+05
metrology      7.002699e+05
cluster        6.735310e+05
dtype: float64


interestingly words like rail increase the budget, so maybe projects associated with infrastructure? we have to keep in mind that the words are lemmatized here. 
Also repurposing and echo suggest projects related to the environment. 
while wafer is clearly correlated to electronic and semiconductor, something the eu is pusing forward to avoid dependency on foreign countries.

## topics 

The project also comes with topics, let's see what we have
There are 491 topics in the dataset.
The top 10 topics are:
HORIZON-MSCA-2023-PF-01-01: 141
HORIZON-MSCA-2022-PF-01-01: 112
HORIZON-MSCA-2021-PF-01-01: 104
ERC-2021-STG: 61
ERC-2023-STG: 60
ERC-2022-STG: 53
ERC-2022-COG: 52
ERC-2023-COG: 47
HORIZON-EIE-2022-SCALEUP-02-02: 46
ERC-2021-COG: 39

90% of the projects are in the top 284 topics
which means there are half of the topics with only a few projects (can be seen from the graph)


### topics and budget 
Let's see if there is a correlation between part of the topics and the budget. By fitting a linear regressor we can see that there are many positive correlation 

Top  Positive Subcalls Impacting Budget
emergency    4.223552e+19
serv         4.223552e+19
cl3          4.223552e+19
tech         4.223552e+19
eosc         4.223552e+19
dev          4.223552e+19
miss         3.478999e+19


 by cheking the https://www.euresearch.ch/en/our-services/inform/open-calls-137.html we can see that:

cl3 (Cluster 3): Horizon Europe is divided into Clusters, and Cluster 3 focuses on Civil Security for Society, covering areas such as disaster resilience, cybersecurity, and border management. This matches your previous mention of cl3 having a positive impact on budgets. Calls like "HORIZON-CL3-2024-CS-01-01" reflect this cluster's focus.


tech (Technology): Horizon Europe also has a strong focus on technology-driven solutions, which likely explains the abbreviation "tech." This could relate to calls focusing on AI, digital solutions, robotics, and space (as seen in "HORIZON-CL4" or "HORIZON-EIC" calls). These technology-driven projects often receive significant funding, reflecting their positive correlation with the budget.

eOSC stands for European Open Science Cloud, an important European initiative aimed at creating an open, federated environment for managing and sharing research data. The EOSC enables researchers to access and reuse data across disciplines and borders
.
Dev most likely refers to development, especially in the context of research and development (R&D).

This likely refers to projects related to services in different contexts. In Horizon Europe, services could encompass digital services, public services, or even AI-enabled services. For example, projects in smart mobility, energy management, or public health often have a significant focus on developing new services to improve efficiency, accessibility, and innovation.


Top 10 Negative topics Impacting Budget
ssri      -4.396994e+19
bm        -4.396994e+19
fct       -4.396994e+19
drs       -4.396994e+19
cs        -4.396994e+19

ssri : Support to Security Research and Innovation 2024 (HORIZON-CL3-2024-SSRI-01) whcih says An identifiable community of EU civil security authorities with common user/functional needs for innovative technology solutions;
Tested and validated capacity of EU technology and industrial base to develop and produce technology prototypes that meet the needs of the EU user community;
Improved delineation of the EU market (including demand and supply) for innovative civil security systems that can articulate alternative options for uptake in function of different industrialisation needs, commercialisation needs, acquisition needs, deployment needs and additional funding needs (beyond R&I funding).

Development of a mature technological solution addressing EU security policy priorities in the areas addressed by the Cluster 3 work programme;
Facilitated access to civil security market for small innovators;
Improved cooperation between public buyers and small supply market actors for a swifter uptake of innovation in response to short to mid-term needs;
Stronger partnerships between small and medium EU security industry and technology actors to ensure the sustainability of the EU innovation capacity in the civil security domain and reduce technological dependencies from non-EU suppliers in critical security areas.


bm is in the Protection and Security (HORIZON) Likely stands for Border Management. Horizon Europe’s Cluster 3 includes border management and security-related projects. The negative correlation could mean that border management projects, while important, are receiving less financial priority compared to other areas like technology, AI, or environmental sustainability.

fct:

Could refer to Fight against Crime and Terrorism, another priority under Cluster 3 in Horizon Europe. Similar to border management, this area may be receiving less funding, particularly when compared to sectors like climate action or technological innovation.

drs : Likely stands for Disaster-Resilient Societies, another key topic within Horizon Europe’s Cluster 3. Despite its importance in building societal resilience against disasters, its negative budget correlation suggests that it might not be receivin

cs:

Cybersecurity or Civil Security: While cybersecurity is crucial, the negative correlation could indicate that certain types of cybersecurity projects (perhaps those focused on niche areas or incremental improvements) receive less funding compared to more transformative or large-scale projects in other sectors, such as AI or climate technologies.


so it seems like the horizon projects in ai are more oriented toward rnd than practical application for fighting crime (good given the ai act and how ai can be used for facial recognition), disaster resilience (ok), and Cybersecurity (this is actually bad bc we ai will improve the the risks of cyber attacks )

## Project similarities

Finally we are here,  we are well aware of what ai horizon project look like and we want to see if our initial assuption is true, i.e. many projects are similar and merging them would save money. 

In order to find similar projects i went with an ai approach (duh!) by using a sentence embeddiner to embed the content of the title and objective. By doing so we can then measure the cosine similarity between these embeddings. Ideally projects that share similar description will be closer together. 

### Similarities

as you can see from the graph above, the mean of similarity is 0.24 which is not so high

Similarity Scores mean: 0.24
Similarity Scores std: 0.12

this is how the scores are distributed. 
Number of similarity scores above 0.95: 2.0
Number of similarity scores above 0.9: 2.0
Number of similarity scores above 0.85: 9.0
Number of similarity scores above 0.8: 37.0
Number of similarity scores above 0.75: 142.0
Number of similarity scores above 0.7: 478.0
Number of similarity scores above 0.6: 4647.0
Number of similarity scores above 0.5: 33350.0

## SentenceTransformer with cosine similarity
The projects with similarity above 0.8 but are 37
The projects with similarity above 0.5 but are 33350
The projects with similarity above 70 but are 478


so, this was an initial filtering. the more advanced one will come later

## Chatgpt

I took inspiration from fineweb and and used a llm (chatgpt gpt-4o) to score the project 0 to 1 based on how much they should merge. I used a promt in the style of fineweb https://huggingface.co/datasets/HuggingFaceFW/fineweb-edu
which is 
```
You are tasked with evaluating the similarity between two research projects and determining whether they should be merged. The projects will be evaluated on five criteria using an additive 5-point scoring system based on how well they satisfy each criterion:

- Add 1 point if the projects share some minor objectives or methods but differ significantly in most areas.
- Add another point if the projects have some overlapping goals, methodologies, or innovations, but also include distinct elements that make them different enough to proceed separately.
- Award a third point if the projects share key similarities in scope, methodology, and innovation but retain enough distinctions to benefit from remaining independent. Resource efficiency may not be substantial, and merging may only yield moderate benefits.
- Grant a fourth point if the projects align closely in scope, methodology, and innovation, and combining them would improve resource efficiency. Merging would likely benefit the overall research output, but they could still function separately with some loss of efficiency.
- Bestow a fifth point if the projects are nearly identical in scope, methodology, and innovation. Merging them would significantly optimize resource use, and keeping them separate would be inefficient.

After scoring each criterion, summarize your analysis in a brief justification, considering the potential benefits of merging and any reasons against merging. Conclude with a structured JSON output containing the parameters "score" and "justification".

The projects:
```PROJ1```

```PROJ2```

```
and then replaced the PROJ1/PROJ2 with the actual json for the project so that the model will have access to the whole info. 

each comparison costs 0,0125252525 eur. 

I ran it for all the pairs that have similarity >=70 (478) but my quota ran out at 316... which are 196 projects ... good enough


### Corr with similarity
First i wanted to investigate if there is a correlation between the merge score and the cosine similarity. 
The correlation between similarity and merge score is 0.14 with a pvalue of 0.0088993

interestingly they don't share much correlation. which means that there could be many more projects that should be merged (according to chatgpt)

### using graph to find connected components

now we are using networkx to find connected components, i.e. cluster of projects that are similar to each other. Out of the 158 project, if we use an edge threshold of 3 (for chatgpt score), we get There are 82 connected components and 35 isolated nodes.
with 4 There are 56 connected components and 102 isolated nodes.
finally with 5 There are 8 connected components and 188 isolated nodes.


#### threshold 3
before checking how much we would save if we merged these projects, we have to see what are the differences in term of budget and duration within each cluster. 
for this we will estimate the avg and std for each cluster and then focus on the std distribution . 



by checking for the std between projects in the same cluster and chunking in milions there are 
There are 6 budget clusters.
0M: 35
1M: 26
2M: 12
3M: 7
4M: 1
11M: 1

which indicates that many project in the same cluster have more or less the same budget

for the duration we have 
There are 19 clusters.
The number of projects in each cluster is:
0 months: 18
1 months: 1
2 months: 1
3 months: 4
4 months: 2
5 months: 2
6 months: 9
7 months: 3
9 months: 9
11 months: 4
12 months: 6
13 months: 3
14 months: 2
15 months: 4
18 months: 10
20 months: 1
21 months: 1
23 months: 1
24 months: 1
There are 53(64.6%) connected projects with a duration std of less than 12 months

interestingly (as you can see from the picture) the distribution heer is mixed, while there are many projects that share the same duration, this is not uniform

##### Saving

So now let's finally see how much we would save if we merge these budgets together. i need a smart way since there are clusters with many budgets, maybe we can say that if a cluster has X project each contribute slightly more then half: (X+1)/2x

with this formula we get 
The total budget of the connected components is 990541834.07 and the total discounted budget is 635428600.55 which is 64.1% of the total budget
The total savings are 355113233.52 which is 0.382% of the total Horizon budget and 5.4% of the total Horizon budget for AI projects


if we instead take only the max between projects i get
The total budget of the connected components is 990541834.07 and the total discounted budget is 438248266.60 which is 44.2% of the total budget
The total savings are 552293567.47 which is 0.594% of the total Horizon budget and 8.5% of the total Horizon budget for AI projects

overall, given that this is the worse consideration, the horizon bugdet is allocated nicely, the worse possible waste is 0.59%, which is very good

#### threshold 5

on the other hand, when the threshold is max (5), the projects are all very similar in budget and duration
The number of projects in each cluster is:
0M: 4
1M: 2
3M: 2
again, very similar std

The number of projects in each cluster is:
0 months: 4
3 months: 1
5 months: 1
6 months: 1
9 months: 1
all of them less than 9 months. well, make sense, these are vey similar

with the fancy formula i get 
The total budget of the connected components is 104943053.95 and the total discounted budget is 76580204.64 which is 73.0% of the total budget
The total savings are 28362849.31 which is 0.030% of the total Horizon budget and 0.4% of the total Horizon budget for AI projects

and the max 
The total budget of the connected components is 104943053.95 and the total discounted budget is 59741284.92 which is 56.9% of the total budget
The total savings are 45201769.03 which is 0.049% of the total Horizon budget and 0.7% of the total Horizon budget for AI projects

well... less than before of course....

#### Considerations
well, we have a range of waste from [28362849, 552293567] from the worse and best considerations. We need to acknoledge tho many limitations of this analysis. 
1. the use of a llm to evaluate if projects should be merged or not is risky and can be a promosing first step to identify potential duplicates, however it should ALWAYS be followed by human (expert) evaluation
2. We saw how the similarity score and chatgpt score do not correlate much.   Someone with more budget than me could run chatgpt on the entire dataset and get different results. ideally we identified 8 projects with merge score 5 out of 196 (4,0816326531%), if the same proportion holds for all the project in the dataset we could be looking at 558 duplicate projects (out of 13674). Again, if the proportion holds, we can be saving a range of [28362849, 552293567]/8 = [3.545.356,125, 69.036.695,875] per project which means a min save of [1.978.308.717,75, 38.522.476.298,25] (*558) which is a much more substantial percentage of the horizon budget [2,0824302292, 40,5499750508]%.
3. Hearing the voices of the experts. In general there is a common sentiment among pp applying and getting these grants that many projects (in ai) have similar scopes and goals, since they are the ones that actually apply, their voices should be taken into account and the issues addressed.