# nba_lineups_prediction

# Los Angeles Lakers 2023 Season Lineup Analysis

### "Which Lineup Combinations Are Most Effective at Driving Team Success?"

**Authors:** Eli Tills & Mihir Sabnis  
**Course:** DSO 579 – Fundamentals of Sports Performance Analytics  
**Instructor:** Lorena Martin, PhD  
**Date:** December 15, 2024

---

## **Project Overview**
This project analyzes the Los Angeles Lakers' 2023 season to identify the most effective lineup combinations for driving team success. By leveraging supervised machine learning models, we evaluate the impact of 5-man and 3-man player combinations on game outcomes (win/loss). The goal is to provide actionable insights into lineup optimization, highlighting player synergies that maximize offensive and defensive performance.

---

## **Objective**
To answer the critical question: **Which lineup combinations are most effective at driving team success?**

---

## **File Descriptions**
- **`3_man.csv`**: Dataset containing stats for all 3-man lineup combinations during the Lakers' 2023 season.
- **`5_man.csv`**: Dataset containing stats for all 5-man lineup combinations during the Lakers' 2023 season.
- **`Match_up_and_date.xlsx`**: Excel file listing game dates, opponents, and win/loss outcomes for the Lakers in the 2023 season.
- **`NBA Lineup Significance Prediction.pptx`**: Presentation summarizing the project’s methodology, findings, and recommendations.
- **`NBA Lineup Significance Prediction.docx`**: Written report detailing the analysis, results, and conclusions of the project.
- **`nba_5-man_player_combo.ipynb`**: Jupyter notebook analyzing the performance of 5-man lineup combinations.
- **`nba_3-man_dummy_lineups.ipynb`**: Notebook implementing dummy variables for 3-man lineups based on their frequency.
- **`nba_3-man_dummy_player.ipynb`**: Notebook using player-level dummy variables to assess individual contributions within 3-man combinations.
- **`nba_5-man_dummy_lineups.ipynb`**: Notebook implementing dummy variables for 5-man lineups.

---

## **Data Collection**
1. **Source:** NBA.com statistics website.
2. **Methodology:**
   - Scraped game data, including win/loss outcomes, opponent details, and dates.
   - Extracted advanced stats for all 5-man and 3-man lineup combinations.
   - Processed 414 unique 5-man lineups and 560+ unique 3-man combinations.
3. **Key Features:** Offensive Rating, Defensive Rating, Net Rating, Assist %, Rebounding Metrics, and Playmaking Stats.

---

## **Data Preparation**
1. **Feature Engineering:**
   - Created binary indicators for player participation in lineups.
   - Normalized and standardized continuous variables.
   - Segmented data into offensive, defensive, and playmaking categories.
2. **Data Splitting:**
   - 80-20 stratified split for training and testing datasets.

---

## **Models Implemented**
1. **Logistic Regression**: Provides baseline predictions and feature interpretability.
2. **Decision Trees**: Captures non-linear relationships and feature importance.
3. **Random Forest**: Handles high-dimensional data efficiently.
4. **XGBoost**: Optimized gradient boosting for high predictive power.

---

## **Evaluation Metrics**
- **Precision**: Minimizes false positives.
- **Recall**: Ensures effective identification of winning lineups.
- **F1-Score**: Balances precision and recall.
- **ROC-AUC**: Evaluates model’s ability to distinguish between wins and losses.

---

## **Key Findings**
1. **5-Man Lineups**:
   - Models struggled to perform significantly better than random guessing.
   - High variability in lineup performance due to inconsistent team dynamics.
2. **3-Man Lineups**:
   - Random Forest achieved the highest AUC-ROC score of 0.89.
   - Key contributors included Taurean Prince and Austin Reaves.
   - Smaller combinations showcased better synergy and predictive power.

---

## **Recommendations**
1. **Team Optimization:**
   - Focus on 3-man combinations for lineup strategy.
   - Utilize real-time model pipelines to adjust lineups pre-game and in-game.
2. **Future Exploration:**
   - Analyze 2-man combinations for identifying dynamic duos.
   - Extend analysis to multiple seasons and other teams for broader insights.
   - Incorporate opponent performance metrics to refine predictions.

---

## **Model Deployment**
Proposed a cloud-based training pipeline for real-time lineup optimization. The system enables dynamic updates using live data, empowering coaches with actionable insights for improving team efficiency.

---

## **Future Improvements**
1. Collect more granular metrics using NBA API for enhanced features.
2. Explore advanced models and hyperparameter tuning for better performance.
3. Evaluate lineup performance over multiple seasons to assess consistency.

---

## **How to Run the Code**
1. Clone the repository:
   ```bash
   git clone <repo-url>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run data preprocessing:
   ```bash
   python preprocess_data.py
   ```
4. Train models:
   ```bash
   python train_models.py
   ```
5. Evaluate results:
   ```bash
   python evaluate_models.py
   ```

---

## **References**
- [NBA.com](https://www.nba.com/)
- Advanced data scraping libraries and open-source APIs for NBA stats.
