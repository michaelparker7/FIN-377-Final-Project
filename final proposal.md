# Research Proposal: Sports Betting Analysis
By Elvin Lee, Michael Parker, and Brandon Smeltz

## Research Question
We are shifting our focus from a broad analysis on every NBA team and player props, to an in-depth analysis on one team. Here, we would be focusing on game to game bets and *not* season long bets. Through this research, our goal is to determine whether or not there are specific props for our chosen team or easily identifiable subsets of these props that consistently outperform the odds sports-betting platforms set. If we are successful, this would be a very profitable opportunity that we have identified. In other words, this project will be focused on the relationship between the different lines you can take as a better given that you take that line every game or for some subset of games that we find most profitable during our project, and how profitable you will become by doing this. For example, we can analyze the Lakers profit amount for the moneyline and based on calculations we make using all of the other variables we have gathered such as the injury list, refs, team strength, etc. determine if taking this moneyline is worth the risk based on our own calculations and the potential profit vs. risk.

Bigger research question: Are there any props for a specified team in the NBA that consistently outperforms the odds sports-betting platforms make and if so what are those props and how can we profit from them?

Specific questions to explore: Is the moneyline, spread, or total points prop profitable for our specified team? Are these props more or less profitable for a specific subset of data such as home or away games? If so, what are these profitable subsets for these props and if they exist how can we maximize profits by using this information.

Hypothesis: One of the original hypotheses we forsee as being the most promising is to look at teams who are deemed the underdog a high percentage of the time, but still manage to win as this would give more profitable individual lines. Given these underdogs is there potentially a subset such as the lakers record being drastically better at home than it is when they play away games that could be paired up with this underdog opportunity to create a profitable situation.

Successful?: We would determine the minimum amount of success as being able to consistently break even and avoid losing any money in the long run. On the other hand the potential for this is almost limitless as very good sports bettors, those who get banned, are able to make a several thousand percent return over a few years and are the ones who have truly mastered how to maximize their profits and know which lines to take.

## Necessary Data
In order to accomplish this problem and have a successful result for our research we will need to obtain several variables for use in our analysis. These variables currently include but are not limited to:

1. Moneyline 
2. Spread
3. Total Points
4. Success Rates for each of these variables
5. Winnings from each of these variables
6. Any other variables we find that may improve profitability through a subset
   - Home vs. Away
   - Win Streak
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

Observations: The 82 regular season games and all of the stats we can scrape for each of these games for our specified team.

Sample Period: This NBA season: 2023-2024 is the season we would like to make predictions for. In testing our model, we could also analyze prior NBA seasons such as the 2022-2023 season in order to better train the model. An interesting avenue this project could take is a machine learning algorithm that learns from the previous season as well as all of the games that have occurred this season to better predict the outcomes of each prop for the rest of the 2023-2024 season. With that being said, our current goal is to focus on relationships between variables and not necessarily make predictions quite yet.

Restrictions: Obtaining this data is very difficult as it is not made publicly available by the sports books. There are several APIs, but they are not free. Currently, we are able to get broad data for our chosen NBA team into an Excel sheet, which we can then take into python, but this is a somewhat brute force method. In doing web scraping, there would be a lot of restrictions, and we are currently hypothesizing the best way to get the data we need.

Necessary Variables: These are listed above.

Variables we'd like: We would like to be able to eventually expand this project and be able to look at player props as well as those for the team, but finding scrapable data may be very difficult. Additionally, we are currently struggling to find data related to injuries that could be used to calculate the team strength.

How we plan to collect more data: We plan to continue searching through as many websites as we can find with usable data and scrape all of the relevant information we can. Like mentioned above, this could prove to be rather difficult as this information isn't made public by the various sports books and often requires the usage of an API.

Storage plan for how we will store data and files within the repository: As mentioned, our plan as of now is to hold most of the betting data in an excel file. If we can find a better method of scraping data directly from a website via a html session request, then we could likely pull all the data at once and store it in a zip file.


## Methodology
Now that we have acqiuired this data, we will need to analyze it and develop a process to get from the raw data to our finished product, hopefully being a profitable subset of props that will maximize our input profits. Our process for achieving this goal is as follows:

1. EDA - see what data variables are missing, which could have errors
2. Clean the data into a format we want - in the testing we've done so far, a lot of the rows have elements that look like this: BOS -1600 or like this: O 216.5. These elements should probably be split into two different columns to make the analysis easier and cleaner.
3. Run regression analyses - to give one particular example, compare odds that the Boston Celtic's win against their actual winning record. Continue to run these regressions searching for high correlations.
5. Create hypothetical returns or portfolios - i.e. if you put 100 dollars into a season long portfolio of the Celtic's winning, how would you have performed. Find which subset of data yields the highest returns.
6. (maybe) create a prediction for future seasons based on these models


** Add how we can use the Machine Learning models such as XG Boost ** 
** Make sure to discuss that we will also be pulling and updating our data set before each game so that only the appropriate info at the time is used for the predictions. ** 



## Financial Application

This project has various financial applications, especially pertaining to this course as it will require a lot of EDA to sort through all of this data and use it to optimize our decisions. We also have to then take our results and weigh the risks with the potential benefits to see if we have actually found anything feasible. 

Additionally, at least 90% of this project will be running regression analyses and seeing where large R^2 values lie. Furthermore, as mentioned previously, this project could be taken down a machine learning path, which obviously has more financial applications.
