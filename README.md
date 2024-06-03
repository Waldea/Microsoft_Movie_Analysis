# Microsoft_Movie_Analysis



**1.0 - Overview**

This report helps to explore what makes a movie successful. We analyze the relationship between movie ratings, movie genres, as well as their total grossing, to identify what are the popular movie genres and to be able to set a target expectation of returns in gross for the first movie produced by Microsoft Cinema.

**2.0 - Business Problem**

Microsoft sees all the big companies creating original video content, and they want to get in on the fun. They have decided to create a new movie studio, but the problem is they don’t know anything about creating movies.

To help better understand the movie industry, our team is charged with exploring what types of films are currently doing the best at the box office. We then translate those findings into actionable insights that the head of Microsoft's new movie studio, Microsoft Cinema, can use to help decide what type of films to create.
**2.1. Questions to consider:**

    Is making movies profitable?
    Popular movie genres?
    Movie budget and target gross?

**3.0 - Data Exploration**

In the folder zippedData in the associated GitHub repository are movie datasets we gathered from:

    Box Office Mojo
    IMDB
    Rotten Tomatoes
    TheMovieDB.org
**
3.1. Dataset selection criteria**

After the initial exploration of the datasets, we have selected 3 datasets:

    imdb.title.basics.csv
    imdb.title.ratings.csv
    tn.movie_budgets.csv

Those datasets were selected based on:

    completeness.
    Relevance.
    Target variables: Average ratings, genres, movie budget, movie gross.

**3.2 Data Cleaning and Preparation
**
The datasets we chose contain thousands of movies and their respective information. The first step before any analysis can be conducted would be to clean the datasets.

**3.2.1 Dealing with missing values
**
Movies with incomplete values or 0 values in budget or grossing are dropped from the dataset as those movies might not be mainstream popular nor would have gross earnings of significance and therefore could be dropped without worrying about significantly altering the analysis.

**3.2.2 Dealing with duplicates**

Next, we identify duplicated movies listed. There could be multiple movies with the same name but are different movies altogether produced by different studios.

Imdb datasets:

    We can identify the duplicates by comparing the original title and the year released.

Tn Movie Budget:

    Duplicates are identified using the production budget and movie gross as keys.

**3.2.3 Data Normalization**

The dataset from *tn.movie_budgets.csv contains important information on production budget and movie gross which is essential for this analysis report. Those columns are cleaned from any commas and $ signs and converted to int.

**3.2.4 Master Dataframe**

After the preparation phase, we combined all 3 datasets into 1 Master dataframe.

After the merge, we found that duplicate movies but different genre values are also an issue, leaving those duplicates in would skew the analysis findings. To remove duplicates, we created a separate dataframe and we considered the number of votes as the key to drop the rows from the Master dataframe since it can be considered that the duplicate with a lower number of votes would be held with a lower opinion.

We repeated all processes above for a final check to ensure a complete dataframe to be exported into a CSV file for analysis.



**6.0 - Analysis Findings
6.1. Is movie making profitable?:**

    The short answer is yes, but other variables should be taken into consideration.
    But there are huge risks to making movies, more than 47% of the movies analyzed are not profitable in a domestic setting.
    And 21.67% of movies listed flopped even after considering worldwide grossing.
    Other variables such as marketing costs which were not included in this analysis, might change how profitable the movies we analyzed are.

Overall making movies can be profitable, but to ensure the continued success of our future movie studio, we should consider how the movies are rated and which genres are most popular.

    We find that most movies made were rated as bad, less than 30% of movies made are rated "Average" and only less than 2% are considered good movies.

**6.2. Movie Gross and Genre Combination
**
To find out what makes a good movie, we analyzed the top 10 most successful movies in movie grossing as well as their average ratings.

Top 10 Grossing Movies and Their Genre Combinations

    The mean worldwide gross is close to $1.43 billion.
    8 out of the top 10 movies contain genres Action and Adventure both making up 26.7% respectively of the 9 identified individual genres.
    Genre combinations classified as Adventure, Action, and Sci-Fi make up 60% of the Top 10 movies.
    The mean worldwide gross is close to $1.43 billion, with the mentioned genre combination dominating above other combinations.

**7.0 - Evaluation
7.1. Budget and Profit Targets**

For the final evaluation, we can set expected targets for the production budget and target gross for what we want to achieve for a successful movie release.

    Production Budget: $22,000,000
    Target Domestic Gross: $527,000,000
    Target Worldwide Gross: $1,430,000,000

**7.2. Recommended Movie Genre**

To be successful and competitive in this colossal movie industry, we have to create a mark for Microsoft Cinema by having a successful first movie produced as the new and upcoming studio.

From the analysis findings we gather, I recommend the following as a guide to what kind of movie the studio should produce:

    Two genres, Action and Adventure have demonstrated consistent success over the last decade in amassing the most amount of gross earnings.
    Sci-fi as a third movie genre is a safe option as 60% of the highest-grossing movies have those 3 combinations.

If the studio wishes to pursue other movie genre combinations;

    Other genres such as animation, comedy, and fantasy can be substituted with Sci-Fi.

Until we can identify which genre the studio can specialize in.

    It is highly recommended that the studio have both Action and Adventure or at least one of them in the movie genre combination as a first release.

**7.3. Future & Further Analysis**

This report does not include several variables for the gathering of the gross earnings of the movies listed in the datasets which may have a high impact on the total earnings of a movie released. Variables for further analysis should include:

    Marketing cost
    Sponsorships
    Royalties


