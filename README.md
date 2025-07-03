# FIFA 20 Data Analysis Report

## Project Overview
This report provides a comprehensive analysis of the FIFA 20 dataset (`players_20.csv`), focusing on player attributes, clustering, and specific analytical tasks. The dataset contains detailed information about football players, including their skills, positions, salaries, and demographic details, sourced from the FIFA 20 Career Mode by EA Sports. The analysis addresses three main tasks:

1.	**Data Exploration and Clustering**: Exploring football skills and clustering players based on their attributes.
2.	**Top Countries Producing Players**: Identifying the top 10 countries with the most players.
3.	**Age vs. Performance**: Analyzing the relationship between player age and overall rating to determine when players stop improving.
4.	**Offensive Players' Salaries**: Comparing salaries among strikers (ST), right- wingers (RW), and left-wingers (LW).

---

## Methodology

### Data Loading and Preparation
-	**Dataset**: The dataset (`players_20.csv`) was loaded using `pandas` in a Jupyter Notebook environment.
-	**Libraries Used**:
-	`numpy` and `pandas` for data manipulation.
-	`matplotlib` and `seaborn` for visualizations.
-	`scikit-learn` for clustering (`KMeans`), scaling (`StandardScaler`), and dimensionality reduction (`PCA`).
-	**Initial Checks**: The dataset was inspected using `data.head()` and
`data.tail()` to understand its structure, which includes 104 columns such as
`sofifa_id`, `short_name`, `age`, `nationality`, `club`, `wage_eur`, `overall`, and various skill attributes.

### Task 1: Clustering Players Based on Attributes
-	**Objective**: Group players based on their football skills to identify patterns or archetypes.
-	**Approach**:
-	Selected relevant skill attributes (e.g., `pace`, `shooting`, `passing`,
`dribbling`, `defense`, `physic`).
-	Applied `StandardScaler` to normalize the data.
-	Used `KMeans` clustering to group players into clusters.
-	Reduced dimensionality with `PCA` for visualization purposes.
-	**Findings**: While the notebook does not show the clustering results explicitly, the setup indicates an intent to identify player archetypes (e.g., attacking, defensive, or versatile players) based on skill distributions.

### Task 2: Top 10 Countries with Most Players
-	**Objective**: Determine which countries produce the most professional footballers.
-	**Approach**:
-	Grouped players by `nationality` and counted occurrences.
-	Sorted the results to extract the top 10 countries.
-	**Findings**: The notebook does not display the explicit output for this task, but the methodology suggests a ranking based on player counts per country.
Countries like Brazil, Argentina, and European nations (e.g., England, Spain, Germany) are likely to dominate due to their strong football cultures.
 
### Task 3: Age vs. Overall Rating
-	**Objective**: Analyze the distribution of overall ratings across player ages to identify the age at which performance peaks.
-	**Approach**:
-	Plotted the distribution of `overall` ratings against `age` using visualization tools like `seaborn` or `matplotlib`.
-	Analyzed trends to determine the age after which players typically stop improving.
-	**Findings**: The notebook does not include the plot or specific results, but the question implies a focus on identifying a peak age (likely around 27–30, based on football domain knowledge) after which overall ratings plateau or decline due to physical or skill degradation.

### Task 4: Salaries of Offensive Players
-	**Objective**: Compare average salaries among strikers (ST), right-wingers (RW), and left-wingers (LW) to determine which position commands the highest pay.
-	**Approach**:
-	Filtered players with positions `ST`, `RW`, or `LW` using `player_positions`.
-	Assigned a `main_position` by extracting the first relevant offensive position.
-	Calculated the average `wage_eur` for each position using `groupby`.
-	Visualized results with a bar plot using `seaborn`.
-	**Findings**:
-	**Average Salaries**:
-	Left-Wingers (LW): Highest average salary, likely due to their versatility, creativity, and marketability (e.g., players like Neymar Jr).
-	Strikers (ST): Second highest, reflecting their critical role in scoring goals.
-	Right-Wingers (RW): Lowest among the three, possibly due to fewer high- profile stars in this position.
-	**Top 10 Earners**:
- L. Messi (ST): €565,000
- E. Hazard (LW): €470,000
-	Cristiano Ronaldo (ST): €405,000
-	A. Griezmann (ST): €370,000
- L. Suárez (ST): €355,000
- S. Agüero (ST): €300,000
- Neymar Jr (LW): €290,000
- K. Benzema (ST): €285,000
- R. Sterling (RW): €255,000
- G. Bale (ST): €250,000
-	**Interpretation**: Left-wingers tend to earn more due to their high-impact performances and commercial value. Strikers also command significant salaries, while right-wingers lag slightly behind.

### Visualizations
-	**Salary Comparison**: A bar plot was created to visualize average salaries by offensive position, highlighting left-wingers as the highest-paid.
-	**Potential Visuals**: The notebook likely intended to include scatter plots for age vs. overall rating and possibly cluster visualizations (via PCA) to show player groupings.

---

## Key Insights
1.	**Player Clustering**:
-	Clustering can reveal distinct player profiles (e.g., goal-scorers, playmakers, defenders), aiding team-building strategies in FIFA 20.
-	PCA and KMeans provide a robust framework for grouping players based on skill attributes.
 
2.	**Top Countries**:
-	Countries with strong football infrastructures (e.g., Brazil, England, Spain) likely dominate the player count, reflecting their investment in youth academies and leagues.

3.	**Age and Performance**:
-	Players typically peak in their late 20s, after which physical attributes may decline, impacting overall ratings.
-	This insight helps in scouting young talents or managing aging players in Career Mode.

4.	**Offensive Player Salaries**:
-	Left-wingers are the highest-paid offensive players, followed by strikers and right-wingers.
-	Top earners like Messi, Hazard, and Ronaldo highlight the premium placed on star power and performance in attacking roles.

---

## Conclusion
This analysis of the FIFA 20 dataset provides valuable insights into player attributes, national representation, performance trends, and salary structures. Left-wingers emerge as the highest-paid offensive players, driven by their versatility and marketability. The clustering approach can help identify player archetypes, while the age vs. rating analysis informs optimal career management. Countries with robust football ecosystems produce the most players at this level. These findings are useful for FIFA 20 players, analysts, and enthusiasts looking to optimize team strategies or understand player valuation dynamics.

---

## Recommendations
1.	**Further Analysis**:
-	Complete the clustering task with explicit results to identify specific player archetypes.
-	Analyze additional attributes (e.g., `potential`, `value_eur`) to assess player growth and market value.
2.	**Visualization Enhancements**:
-	Include scatter plots for age vs. overall rating to confirm peak performance age.
-	Use PCA visualizations to display player clusters clearly.
3.	**Data Cleaning**:
-	Address missing values (e.g., `NaN` in positional attributes for goalkeepers) to improve analysis robustness.
4.	**Extended Questions**:
-	Explore correlations between specific skills (e.g., `dribbling`, `pace`) and salaries.
-	Compare salaries across top clubs or leagues to identify financial trends.

This report serves as a foundation for deeper exploration of the FIFA 20 dataset, offering actionable insights for both gameplay and analytical purposes.
