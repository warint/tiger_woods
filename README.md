# tiger_woods

This repo contains a comprehensive list of Tiger Woods' speeches, which he gave during his tournaments' participation. Some sentiment scores have been computed using various Natural Language Processing techniques.

## Cite

Please cite as :

@article{PASTORIZA2022107955,
title = {Dataset of two decades of Tiger Woods press conferences and tournament performance},
journal = {Data in Brief},
volume = {41},
pages = {107955},
year = {2022},
issn = {2352-3409},
doi = {https://doi.org/10.1016/j.dib.2022.107955},
url = {https://www.sciencedirect.com/science/article/pii/S2352340922001664},
author = {David Pastoriza and Thierry Warin},
keywords = {Tiger Woods, Press conferences, Sentiment analysis, Natural language processing, Machine learning},
abstract = {This data article describes a dataset that allows exploring the determinants of superstars’ sentiment in tournaments. It consists of 1,284 press conferences of Tiger Woods in the PGA Tour between 1996 and 2020. We used natural language processing, a form of artificial intelligence, to extract and encode in a quantitative form the sentiment in Tiger Woods press conferences both before the tournament and after the rounds played. Additionally, the dataset provides a series of variables that describe Tiger Woods’ scoring and performance momentum in each round and variables that describe health-related and off-the-course issues that could affect his performance on the course. This data can be useful to understand the sentiment that superstars go through before important tournaments, their sentiment following a major victory or defeat, how that sentiment evolves throughout their athletic career, and how sentiment is associated with performance momentum.}
}

## Description of the variables in the dataset

| Variable | Type | Description |
|----------|------|-------------|
| Tournament_Year | Numeric | Yearly season |
| Tournament_Order | Ordinal | Chronological order of tournaments within a season (i.e., smaller numbers took placer earlier in the season) |
| Permanent_Tournament_Number | Numeric | 	Identification number that is unique to that tournament, regardless of the sponsor/name of the tournament that may change over the years |
| Course_Number | Numeric | Course number that does not change over time (i.e., different tournaments may be played on the same course) |
| Player_Number | Numeric | Player identification number. Does not change over the years |
| Round_Number | Numeric | Round number. PGA Tour tournaments generally have four rounds |
| Event_Name | Numeric | Name of the tournament |
| Course_Name | Text | Name of the course in which the tournament took place |
| Interview_Text | Text | The integral text of the interview |
| Number_Of_Answers | Numeric | Number of answers provided by Tiger Woods during the Q&A section |
| Link | Text | Link to the original document (redirecting on ASAP Transcription website) |
| Response_Negative | Numeric | The negative score computed on Tiger Woods’ responses |
| Response_Positive | Numeric | The positive score computed on Tiger Woods’ responses |
| Response_Sentiment | Numeric | The subtraction between the positive and the negative scores computed on Tiger Woods’ responses |
| Round_Score | Numeric | Number of strokes of the round |
| End_of_Round_Pos_numeric_ | Ordinal | Player's rank in the round (i.e., 1 means he is leading the tournament, 2 means he is the runner-up, etc.) |
| Total_Holes_Over_Par | Numeric | Number of holes in the round in which the player scored bogey or worse in the round |
| Birdies | Numeric | Number of birdies in the round |
| Birdies_Rank | Ordinal |  Players' rank in number of birdies in the round (i.e., 1 means he was the player with the highest number of birdies in the round)|
| Bogey_Avoidance_Rank | Ordinal | Player's rank in terms of the number of holes in which the player saved a situation of bogey in the round |
| Driving_Distance_Rank | Ordinal | Player's rank in driving distance in the round |
| Driving_Accuracy_Rank | Ordinal | Player's rank in driving accuracy in the round |
| GIR_Rank | Ordinal | Player's rank in number of greens in regulation in the round |
| Scrambling_Rank | Ordinal | Player's rank in scrambling in the round (i.e., ability to recover from difficult situations) |
| Distance_to_leader_strokes | Numeric | Distance in strokes to the interim leader at the end of the round (i.e., if Tiger is trailing by two shots, it takes value 2; if Tiger is leading, the variable takes value 0) |
| Distance_to_leader_ranks | Numeric | Distance in ranks to the interim leader at the end of the round (i.e., if Tiger is in rank 3, it takes value 2; if Tiger is leading, it takes value 0) |
| Ranks_gained | Numeric | Equal to the rank at the end of Roundn minus the rank at the end of Roundn-1. For instance, if Tiger had a position 3 at the end of Roundn and 5 at the end of Roundn-1, the variable's value is −2. It takes missing values for round 1 |
| Strokes_gained_v_a_v_Leader | Numeric | Equal to distance to the leader (in strokes) at the end of Roundn minus distance to the leader (in strokes) at the end of Roundn-1. It takes missing values for round 1 |
| Distance_to_runner_up_strokes_ | Numeric | Distance in strokes to the interim runner-up at the end of the round. For instance, if Tiger is leading by two shots, the variable should take value 2; if Tiger is co-leading, the variable should take value 0; if Tiger is neither leading nor co-leading, it takes missing value. |
| Strokes_gained_v_a_v_Runner_up | Numeric |  Distance in strokes to runner-up at the end of Roundn minus distance to runner-up at the end of Roundn-1. Note that this variable should have a missing value for observations of round 1. Note that this variable should have a missing value when Tiger is not leading.|
| Injury | Categorical {1; 0} | Tiger had a minor injury when he entered the event |
| Major_injury_surgery | Categorical {1; 0} | Tiger Woods had a major injury when he entered the event |
| Personal_issues | Categorical {1; 0} | Tiger Woods had personal issues when he entered the event |
| Major | Categorical {1; 0} | Takes value 1 if tournament is a major (i.e., prestigious) |
| Prize_Money | Numeric | Prize money of the tournament |
| SoF | Numeric | Strength of the field of players in the tournament (i.e., the higher the number, the more competitive is the field) |
| OWGR | Numeric | OWGR of Tiger at the moment of the observation |
| url | Text | Link to the website from which the text is scraped |
| year | Numeric | Year of the tournament |
| Permanent_Tournament_Number | Numeric | Unique tournament identifier across years |
| Round_Number | Ordinal | Counter var for the round within each tournament |
| Interview_Text | Text | Scraped text that is analyzed |
| speech | Ordinal | Counter var for the nth article within a given year |
| fullart_bing_positive | Numeric | Positive sentiment score of the full article using the "Bing" dictionary |
| fullart_bing_negative | Numeric | Negative sentiment score of the full article using the "Bing" dictionary |
| fullart_bing_sentiment | Numeric | Overall sentiment score of the full article using the "Bing" dictionary (calculated by subtracting the negative score from the positive score) |
| fullart_afinn_positive | Numeric | Positive sentiment score of the full article using the "Afinn" dictionary |
| fullart_afinn_negative | Numeric | Negative sentiment score of the full article using the "Afinn" dictionary |
| fullart_afinn_sentiment | Numeric | Overall sentiment score of the full article using the "Afinn" dictionary (calculated by subtracting the negative score from the positive score) |
| fullart_nrc_positive | Numeric | Positive sentiment score of the full article using the "NRC" dictionary |
| fullart_nrc_negative | Numeric | Negative sentiment score of the full article using the "NRC" dictionary |
| fullart_nrc_sentiment | Numeric | Overall sentiment score of the full article using the "NRC" dictionary (calculated by subtracting the negative score from the positive score) |
| resp_bing_positive | Numeric | Positive sentiment score of the player responses in an article using the "Bing" dictionary |
| resp_bing_negative | Numeric | Negative sentiment score of the player responses in an article using the "Bing" dictionary |
| resp_bing_sentiment | Numeric | Overall sentiment score of the player responses in an article using the "Bing" dictionary (calculated by subtracting the negative score from the positive score) |
| resp_afinn_positive | Numeric | Positive sentiment score of the player responses in an article using the "Afinn" dictionary |
| resp_afinn_negative | Numeric | Negative sentiment score of the player responses in an article using the "Afinn" dictionary |
| resp_afinn_sentiment | Numeric | Overall sentiment score of the player responses in an article using the "Afinn" dictionary (calculated by subtracting the negative score from the positive score) |
| resp_nrc_positive | Numeric | Positive sentiment score of the player responses in an article using the "NRC" dictionary |
| resp_nrc_negative | Numeric | Negative sentiment score of the player responses in an article using the "NRC" dictionary |
| resp_nrc_sentiment | Numeric | Overall sentiment score of the player responses in an article using the "NRC" dictionary (calculated by subtracting the negative score from the positive score) |
| quest_bing_positive | Numeric | Positive sentiment score of the journalist's questions in an article using the "Bing" dictionary (calculated as the positive sentiment score of the full article minus the positive sentiment score of the responses) |
| quest_bing_negative | Numeric | Negative sentiment score of the journalist's questions in an article using the "Bing" dictionary (calculated as the negative sentiment score of the full article minus the negative sentiment score of the responses) |
| quest_bing_sentiment | Numeric | Overall sentiment score of the journalist's questions in an article using the "Bing" dictionary (calculated as the overall sentiment score of the full article minus the overall sentiment score of the responses) |
| quest_afinn_positive | Numeric | Positive sentiment score of the journalist's questions in an article using the "Afinn" dictionary (calculated as the positive sentiment score of the full article minus the positive sentiment score of the responses) |
| quest_afinn_negative | Numeric | Negative sentiment score of the journalist's questions in an article using the "Afinn" dictionary (calculated as the negative sentiment score of the full article minus the negative sentiment score of the responses) |
| quest_afinn_sentiment | Numeric | Overall sentiment score of the journalist's questions in an article using the "Afinn" dictionary (calculated as the overall sentiment score of the full article minus the overall sentiment score of the responses) |
| quest_nrc_positive | Numeric | Positive sentiment score of the journalist's questions in an article using the "NRC" dictionary (calculated as the positive sentiment score of the full article minus the positive sentiment score of the responses) |
| quest_nrc_negative | Numeric | Negative sentiment score of the journalist's questions in an article using the "NRC" dictionary (calculated as the negative sentiment score of the full article minus the negative sentiment score of the responses) |
| quest_nrc_sentiment | Numeric | Overall sentiment score of the journalist's questions in an article using the "NRC" dictionary (calculated as the overall sentiment score of the full article minus the overall sentiment score of the responses) |
| sentimentr_fullart | Numeric | Sentiment of the full article using R's sentimentr package |
| sentimentr_resp | Numeric | Sentiment of the player responses using R's sentimentr package |
| sentimentr_quest | Numeric | Sentiment of the journalist's questions using R's sentimentr package (calculated as the sentimentr score of the full article sentimentr minus sentimentr score of the responses) |
