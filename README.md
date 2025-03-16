# Dating-Algorithm-Analysis-with-R
Analyzed the effectiveness of Oz's dating algorithm by calculating liking and match scores using correlation-based recommendations to identify potential algorithmic errors.

![image](https://github.com/user-attachments/assets/417bfecf-3f30-4827-a2b8-0efcd19a0f82)

## Project Background

The Oz dating app employs a unique matching system that pairs users for brief video chats based on calculated "Liking Scores" derived from user preferences. Recently, Oz engineers noticed a decrease in match rates, suggesting a possible algorithm bug. This project evaluates Oz's algorithm's accuracy in predicting matches using correlation-based calculations.

## Problem Statement

Oz’s algorithm predicts matches using calculated "Liking Scores" and "Match Scores" based on correlation patterns in user preferences. This study aims to:

Verify the correctness of Oz’s algorithm by recalculating the Liking and Match Scores.

Identify discrepancies in calculated matches to determine if the algorithm is bugged.

## Key Questions

Does Oz's algorithm accurately predict matches?

Are the identified pairs aligned with calculated match scores?

If mismatches are found, what insights can improve the algorithm?

## Data Overview

The dataset includes two key matrices:

Liked_M_F: Details whether men “liked” women (rows = men, columns = women).

Liked_F_M: Details whether women “liked” men (rows = women, columns = men).

Other key variables:

Liking Score: Score representing how much a user is likely to “like” another person.

Match Score: Combined Liking Scores between pairs, representing overall compatibility.

## Methodology

Data Preparation: Loaded the data and prepared matrices for accurate correlation analysis.

Liking Score Calculation: Used correlation thresholds (≥ 0.15 or ≤ -0.15) to identify comparison users and weighted their influence using absolute correlation values.

Match Score Calculation: Added calculated Liking Scores from both perspectives to assess mutual interest.

Result Analysis: Compared calculated match scores with Oz’s suggested matches to identify discrepancies.

## Key Findings & Insights

### 1. Algorithm Accuracy in Predicting Matches

Oz’s suggested matches failed to align with the highest Match Scores in the dataset.

Anna & Kristoff, Elphaba & Fiyero, and Rosie & Bruno were the correct matches based on the recalculated scores, contradicting Oz’s predictions.

![image](https://github.com/user-attachments/assets/c3202cf9-d01b-4531-8248-d67873572078)


### 2. Identifying the Bug

The algorithm incorrectly paired some users, likely due to issues in the correlation filtering logic or incorrect weighting in score calculations.

The recalculated Liking Scores provided more consistent and logical pairings.
![image](https://github.com/user-attachments/assets/8f8f8519-c943-46b8-a940-95ad2191a68c)


## Conclusion

The analysis found that Oz’s algorithm produced incorrect matches, confirming the presence of a bug. Correct pairings identified through recalculated scores highlight the importance of refining correlation logic and score weighting to improve matchmaking accuracy.

## Recommendations

Revise Oz's matching algorithm to ensure Liking Scores are calculated with consistent weighting logic.

Implement improved correlation thresholds to better identify meaningful user preferences.

Conduct further testing across broader datasets to enhance model robustness.
