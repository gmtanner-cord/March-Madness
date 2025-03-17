# March-Madness
NCAA March Madness Basketball Data

Men's Tournament data for 2001-2024 (excluding 2020).
Women's Tournament data (coming soon)

## The Data
Data was collected from
[Sports-Reference](https://www.sports-reference.com/cbb/)
for the NCAA Men's basketball tournaments from 2001-2024 (no tourney in
2020). The data was collected by official scorers at the college
basketball games. One flaw in the data is that the season stats also
include the performance in the NCAA tournament. This does affect its
predictive ability for trying to predict the results of a future
tournament, but it would be a lot more work to fix the data.

There are 134 variables in the dataset (2 response variables, 
2 variables about for the round and year, and 
65 for each team with ".1" appended for team 1 and ".2" appended for team 2). 
Here are some of the predictor variables:

-   seed: Number 1-16. Determined by a 10-person committee. Lower seeds
    are better.
-   win_pct: Win Percentage (total, home, away, conf). Calculated as
    wins over games played.
-   srs: Simple Ratings System. A rating that takes into account average
    point differential and strength of schedule. The rating is
    denominated in points above/below average, where zero is average.
    Non-Division I games are excluded from the ratings.
-   sos: Strength of Schedule. A rating of strength of schedule. The
    rating is denominated in points above/below average, where zero is
    average. sos is srs minus the team's average point differential.
-   pts_pg: Points per Game. Number of points scored divided by number
    of games.
-   opp_pts_pg: Opponents Points per Games. Number of points scored by
    opponents divided by number of games.
-   pace: An estimate of number of possessions per 40 minutes.
-   off_rtg: Offensive rating. Points scored per 100 possessions.
-   fg_pct, fg3_pct, ft_pct: Field Goals (2 points), 3-Point Field
    Goals, Free Throw (1 point) percentages. Number scored divided by
    number attempted.
-   \*\_pg: Counting Stats per Game, including field goals (fg), 3-Point
    Field Goals (fg3), Free Throw (ft), offensive rebounds (orb), total
    rebounds (trb), assists (ast), steals (stl), blocks (blk), turnovers
    (tov), and personal fouls (pf).
-   \*\_opp: Variables that denote the amount of that stat for the team's opponents.
-   conf: Conference
-   mp_bench_pct, pts_bench_pct: Percent of minutes played/points scored by the bench players (players ranked 6th or more by minutes played)
-   height_avg, height_max: Average and max height of players of the top 6 players (by minutes played) on the roster.
-   exp_avg: Average experience (Freshman = 1 year, ..., Senior = 4 years) of the top 6 players (by minutes played) on the roster.
-   rsci_pct: Percentage of players ranked by RSCI during their senior year of high school of the top 6 players (by minutes played) on the roster.
-   min_return, pts_return: Percent of minutes played/points scored returned from previous year's squad.

There are two response variables:

-  winner: has values "team1" and "team2" for which team won the game.
-  point_diff: difference of scores team1-team2 in the game

The dataset has been mirrored so that each game shows up twice, once
with each of the teams as team 1. This was done to alleviate the bias in
the data towards team 1 winning (typically the better seed was listed
first as team 1 in the early rounds of the bracket) and to make your
classifiers robust to the order of the teams (you wouldn't want to model
to produce different predictions based on which team was listed as team
1).
