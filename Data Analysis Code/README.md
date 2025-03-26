Sports Anxiety Intervention Analysis Code

Overview
This R Markdown notebook analyzes the effectiveness of coaching behaviours intervention program on athletes' anxiety across three stages of a competitive season (Pre-Season, Mid-Season, and Post-Season). The analysis compares a control group (no intervention) with an experimental group (receiving intervention) across three anxiety dimensions: Somatic Score, Worry Score, and Concentration.

How to Use
1. Run chunks sequentially to reproduce analysis
2. Modify sample size or score parameters in initial chunks to explore different scenarios
3. Adjust visualization parameters for custom plots

# 1. Data Simulation
Since there is no actual participant, we use data simulating to get some examples for our analyzing. 
- Simulates datasets for both control and experimental groups (n=35 each)
- Generates normally distributed scores (range 4-20) for three anxiety measures
- Each participant is measured at three time points (Pre/Mid/Post-season)

# 2. Data Cleaning
- Removes participants with:
  - Missing data at any stage
  - Scores outside valid range (4-20)
- Creates cleaned datasets for both groups

# 3. Exploratory Analysis
- Calculates descriptive statistics (means, SDs) for each measure at each stage
- Visualizes score distributions via boxplots
- Combines scores into Total Anxiety Score for each participant

# 4. Statistical Analysis
- Two-way ANOVA to examine:
  - Main effects of Group (Control vs. Experimental)
  - Main effects of Stage (Pre/Mid/Post)
  - Group × Stage interaction
- Post-hoc tests (LSD) for pairwise comparisons between groups at each stage

# 5. Visualization (Using "ggplot")
- Bar plots showing mean total scores with error bars
- Significance markers for group comparisons at each stage


Key Findings
1. Significant Group Differences: The intervention showed significant effects in reducing anxiety scores
2. Stage-Specific Effects: 
   - Strongest effects in Pre-Season (p < .0001)
   - Non-significant differences in Mid- and Post-Season
3. Visual Patterns: Experimental group consistently showed lower anxiety scores across all stages


Interpretation Notes
- Results suggest intervention is most effective when implemented early in season
- Non-significant later effects may indicate need for booster sessions
- Practical significance should be considered alongside statistical significance