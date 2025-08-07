<h1>College Football Preseason Ranking Predictions</h1>

<h2>Description</h2>
This project predicts preseason AP Top 25 rankings using team offensive statistics and historical poll data from 2014 to 2024. The dataset combines scraped NCAA team performance metrics along with manually collected preseason AP and Coaches Poll rankings. The goal is to explore whether past performance and basic offensive stats can be predictive of preseason media expectations.
This notebook demonstrates scraping, data cleaning, merging multiple sources, and preparing data for machine learning models. The final output is a merged dataset suitable for regression or ranking prediction modeling.

<h2>Languages and Libraries Used</h2>

- <b>Python</b>  
- <b>Pandas</b>  
- <b>NumPy</b>  
- <b>BeautifulSoup</b>  
- <b>Requests</b>  

<h2>Environments Used</h2>

- <b>Google Colab</b>  
- <b>Jupyter Notebook</b>  
- <b>Python 3.11+</b>

<h2>Data Sources</h2>

- <b>Historical Rankings Dataset (2015-2024):</b>

    - Manually compiled dataset combining preseason Coaches Poll ranks and AP Poll ranks across ten seasons (2015-2024), stored in combined_team_stats_and_polls.csv
 
      - Source URLs:

          - [AP Poll Archives](https://www.sports-reference.com/cfb/years/)
       
          - [ESPN College Football Polls](https://www.espn.com/college-football/rankings)
      

<h2>Models Implemented</h2>

- <b>Random Forest Regressor:</b> Trained using Preseason_Coaches_Rank as input and Preseason_AP_Rank as target

- <b>Scatter Plot Visualization:</b> Coaches Poll vs. Predicted AP Poll for 2025, including a reference line to indicate perfect agreement

- <b>Team Comparison Analysis:</b> Merged predicted AP rankings with the 2024 final AP poll to measure rank movement ("Change")

- <b>CSV Outputs:</b>

    - predicted_ap_preseason_top25_2025.csv: The predicted AP ranks for 2025
 
    - 2025_ap_vs_2024_final_comparison.csv: Predicted AP rank vs. 2024 final rank with computed change
 
- <b>Plot Output:</b>

    - 2025_ap_vs_coaches_plot.png: Scatter plot of Coaches vs. Predicted AP rankings
 
<h2>Metric Summary</h2>

- Predictions are based solely on Coaches Poll ranks, modeling how historically similar data translated to AP poll results

- The model assumes rank-based relationships are consistent year to year and doesn't include deeper team performance metrics

- Rank changes are computed as:

    - Change = Final_AP_Rank_2024 - Predicted_AP_Preseason_Rank_2025
 
       - Positive: Expected rise
     
       - Negative: Expected Drop
     
<h3>Example Output Summary:</h3>

- <b>Top 10 Projected Risers:</b> Teams that are predicted to rank significantly higher in the 2025 preseason AP poll compared to where they finished in 2024
  
- <b>Top 10 Projected Fallers:</b> Teams that are expected to drop in the AP rankings relative to last season's final standings

<h2>Visualizations</h2>

<p align="center">

<b>2025 Coaches vs. Predicted AP Rank</b><br/>
<img src="https://imgur.com/a/2Lbjkct.png" width="80%" alt="Coaches vs. Predicted AP Rank"/>
