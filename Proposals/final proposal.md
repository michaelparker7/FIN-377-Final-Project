# Research Proposal: Sports Betting Analysis
By Elvin Lee, Michael Parker, and Brandon Smeltz

## Research Question
We are shifting our focus from a broad analysis on every NBA team and player props, to focusing on the moneylines and team totals for a select few teams. We will select a title contending team, a middle of the pack team, and a bottom team, to see which type of teams make the most sense *(according to our model)* betting on. Through this research, our goal is to determine whether or not the moneylines/team totals for our chosen teams can consistently outperform the odds sports-betting platforms set. If we are successful, this would be a very profitable opportunity that we have identified. In other words, this project will be focused on the finding a way to quanitify a win probability, and compare its relationship to the implied odds you get as a better through the sportsbooks. We will be betting every game for our subset of teams, and we will be taking both sides of the win as well as both over and under on the team totals. If some games present the chance to bet on an underdog, when the win probability > implied odds, we plan on deteremining a way to manipulate our bet size as a ratio of our unit size to mitigate risk. For example, when looking at a bad team, it is not sound to continue to bet against them, as the profits are minimal. Rather, we wish to find potential spots where it could be profitable to bet on the underdog. Our title contending teams will deal with the issues of betting on games with huge favorites and underdogs, while our analysis on the middle of the pack team will help us gain a more balanced understanding of betting NBA games. For example, we can analyze the Lakers profit amount for the moneyline and based on calculations we make using all of the other variables we have gathered such as the injury list, refs, team strength, etc. determine if taking this moneyline is worth the risk based on our own calculations and the potential profit vs. risk.

Bigger research question: Are there any props for a specified team in the NBA that consistently outperforms the odds sports-betting platforms make and if so what are those props and how can we profit from them? When is the right time to bet on the underdogs? Are there identifiable varaibles that contribute to the sucess of predicting over/under on a team total or a team cashing their money line?

Specific questions to explore: Are the moneyline and total points prop profitable for our specified team? Are these props more or less profitable for a specific subset of data such as home or away games? If so, what are these profitable subsets for these props and if they exist how can we maximize profits by using this information? When looking at high scoring games, is there data that supports this, or should we take into account hot/cold streaks nba teams go through during a season?

Hypothesis: One of the original hypotheses we forsee as being the most promising is to look at teams who are deemed the underdog a high percentage of the time, but still manage to win as this would give more profitable individual lines. Given these underdogs is there potentially a subset such as the lakers record being drastically better at home than it is when they play away games that could be paired up with this underdog opportunity to create a profitable situation.

Successful?: We would determine the minimum amount of success as being able to consistently break even and avoid losing any money in the long run. On the other hand the potential for this is almost limitless as very good sports bettors, those who get banned, are able to make a several thousand percent return over a few years and are the ones who have truly mastered how to maximize their profits and know which lines to take.

## Necessary Data
In order to accomplish this problem and have a successful result for our research we will need to obtain several variables for use in our analysis. These variables currently include but are not limited to:

1. Moneyline/ Team total line and odds
2. Box Scores
3. NBA schedules
4. NBA player/team stats
5. Success Rates for each of these variables
6. Winnings from each of these variables
7. Any other variables we find that may improve profitability through a subset
   - Home vs. Away
   - Hot/Cold Streak
   - Record in Last 10 games
   - Conference game/ or not
   - Reffing staff
   - Injuries
   - Team Strength on a given night which contains
     - The quantity of PPG missing due to injury compared to the additional PPG added by the replacement starters
     - How far the team traveled since their last game
     - How much time the team had since their last game
     - Did they get to see family?
     - Net scoring margin in recent games
     - Win streak

Observations: The regular season games during October - March and all of the stats we can scrape for each of these games for our specified team.

Sample Period: This NBA season: 2023-2024 from October through the end of March. The end of March marks the culmination of the regular season, where the few remaining games to are extremely intense due to playoff implications, or extremely loose, as teams have already been eliminated from contention. These games may serve as outliers, and are removed from consideration. In testing our model, we could also analyze prior NBA seasons such as the 2022-2023 season in order to better train the model. An interesting avenue this project could take is a machine learning algorithm that learns from the previous season as well as all of the games that have occurred this season to better predict the outcomes of each moneyline for the rest of the 2023-2024 season. With that being said, our current goal is to focus on relationships between variables and not necessarily make predictions quite yet.

Restrictions: Obtaining this data is very difficult as it is not made publicly available by the sports books. There are several APIs, but they are not free. Currently, we are able to get broad data for our chosen NBA team into an Excel sheet, which we can then take into python, but this is a somewhat brute force method. In doing web scraping, there would be a lot of restrictions, and we are currently hypothesizing the best way to get the data we need.

Necessary Variables: These are listed above.

Variables we'd like: We would like to be able to eventually expand this project and be able to look at player props as well as those for the team, but finding scrapable data may be very difficult. Additionally, we are currently struggling to find data related to injuries that could be used to calculate the team strength.

How we plan to collect more data: We plan to continue searching through as many websites as we can find with usable data and scrape all of the relevant information we can. Like mentioned above, this could prove to be rather difficult as this information isn't made public by the various sports books and often requires the usage of an API.

Storage plan for how we will store data and files within the repository: As mentioned, our plan as of now is to hold most of the betting data in an excel file. If we can find a better method of scraping data directly from a website via a html session request, then we could likely pull all the data at once and store it in a zip file.


## Methodology
Now that we have acqiuired this data, we will need to analyze it and develop a process to get from the raw data to our finished product, hopefully being a profitable subset of props that will maximize our input profits. Our process for achieving this goal is as follows:

1. EDA - see what data variables are missing, which could have errors
2. Clean the data into a format we want - in the testing we've done so far, a lot of the rows have elements that look like this: BOS -1600 or like this: O 216.5. These elements should probably be split into two different columns to make the analysis easier and cleaner.
3. Create a running statsheet - we must add new stats from box scores into our running stat sheet of averages to make sure our model can only see historical data
4. Run regression analyses - go through box scores to determine which specific stats contribute to team sucess or high/low scoring.
5. Run Machine learning - X_train is the information given before the game (team stats, team strength, player stats, injuries), and y_train is the results of the games, along with the box score which is then updated into our running statsheet. Our test data will be focused on games played by our select teams past Jan 1, 2024, which marks nearly the halfway point in the NB We plan to use XG Boost, as this ML model is great at understanding confusing relationships and highlights the importance of specific variables. 
6. Create hypothetical returns or portfolios - Each team will have their own return portfolios (one for moneylines and one for team totals) for when betting on their games. Do an analysis on which subset of data yields the highest returns and why.
7. (maybe) create a prediction for upcoming playoff games based on these models




## Financial Application

This project has various financial applications, especially pertaining to this course as it will require a lot of EDA to sort through all of this data and use it to optimize our decisions. We also have to then take our results and weigh the risks with the potential benefits to see if we have actually found anything feasible. 

Additionally, a large portion of this project will be of this project will be running regression analyses and finding strong correlating variables. Furthermore, as mentioned previously, this project could be taken down a machine learning path, which obviously has more financial applications.
