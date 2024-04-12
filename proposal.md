# Research Proposal: Sports Betting Analysis
By Elvin Lee, Michael Parker, and Brandon Smeltz

## Research Question
Through this research, our goal is to determine whether or not there are teams in the NBA that consistently outperform the odds sports-betting platforms make. The hope that we will be able to find a specific prop that consistently outperforms the odds or atleast an easily attainable subset for a prop that will achieve this goal. If we are successful this would be a very profitable opportunity that we have identified. In other words, this project will be focused on the relationship between the different lines you can take as a better given that you take that line every game or for some subset of games that we find most profitable during our project, and how profitable you will become by doing this. For example, we can analyze each of the 30 teams in the NBA and look at the win percentage and winning amount for moneyline, spread, total points, etc... for each of these scenarios.

Bigger research question: Are there any props for any teams in the NBA that consistently outperform the odds sports-betting platforms make and if so what are they and how can we profit from them?

Specific questions to explore: Is the moneyline, spread, or total points prop profitable for any team? Are these props more profitable for a specific subset of data. If so, what is this subset and if it exists how can we maximize the profits by using this information.

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

Observations: Each of the 30 NBA teams and each of their respective props

Sample Period: This NBA season: 2023-2024. In testing our model, we could also analyze prior NBA seasons. An interesting avenue this project could take is a machine learning algorithm. For example, build a model based on the 2000 season and test it on the 2001 season. Then, refine the model and test it on the 2002 season, and so on. However, as of now, our goal is to focus on relationships and not necessarily predictions.

Restrictions: Obtaining this data is very difficult as it is not made publicly available by the sports books. There are several APIs, but they are not free. Currently, we are able to get broad data from all 30 NBA teams into an Excel sheet, which we can then take into python, but this is a somewhat brute force method. In doing web scraping, there would be a lot of restrictions, and we are currently hypothesizing the best way to get the data we need.

Necessary Variables: These are listed above.

Variables we'd like: We would like to be able to eventually expand this project and be able to look at player props as well as those for the teams, but finding scrapable data may be very difficult.

How we plan to collect more data: We plan to continue searching through as many websites as we can find with usable data and scrape all of the relevant information we can. Like mentioned above, this could prove to be rather difficult as this information isn't made public by the various sports books.

Storage plan for how we will store data and files within the repository: As mentioned, our plan as of now is to hold most of the betting data in an excel file. If we can find a better method of scraping data directly from a website via a html session request, then we could likely pull all the data at once and store it in a zip file.


## Methodology
Now that we have acqiuired this data, we will need to analyze it and develop a process to get from the raw data to our finished product, hopefully being a profitable subset of props that will maximize our input profits. Our process for achieving this goal is as follows:

1. EDA - see what data variables are missing, which could have errors
2. Clean the data into a format we want - in the testing we've done so far, a lot of the rows have elements that look like this: BOS -1600 or like this: O 216.5. These elements should probably be split into two different columns to make the analysis easier and cleaner.
3. Run regression analyses - to give one particular example, compare odds that the Boston Celtic's win against their actual winning record.
4. Continue running these regressions searching for high correlations
5. Create hypothetical returns or portfolios - i.e. if you put 100 dollars into a season long portfolio of the Celtic's winning, how would you have performed
6. (maybe) create a prediction for future seasons based on these models



## Financial Application

This project has various financial applications, especially pertaining to this course as it will require a lot of EDA to sort through all of this data and use it to optimize our decisions. We also have to then take our results and weigh the risks with the potential benefits to see if we have actually found anything feasible. 

Additionally, at least 90% of this project will be running regression analyses and seeing where large R^2 values lie. Furthermore, as mentioned previously, this project could be taken down a machine learning path, which obviously has more financial applications.
