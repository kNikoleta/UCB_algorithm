# News Article Recommendation Using Modified UCB Algorithm

## Overview

This project focuses on recommending news articles to users in a way that maximizes the clickthrough rate (CTR). The goal is to choose a news article for each user to maximize the chance that the user clicks on it to read further. The problem is formalized as follows:

- **News Articles**: There are \(K\) news articles available to recommend.
- **Users**: Each user has specific characteristics: gender (male or female) and age group (under or over 25).
- **User Preferences**: Different types of users have different click probabilities for the articles.

The algorithm maximizes the total number of clicks over \(T\) rounds, given the unknown click probabilities and user preferences.

## Problem Setup

### User Characteristics
- **Gender**: Male or Female
- **Age Group**: Under 25 or Over 25
- Users are drawn independently and identically distributed (IID) with initially assumed equal probability.

## Algorithm

### Modified UCB Algorithm
The proposed algorithm modifies the standard UCB to account for user types:
1. Maintain separate counts and estimates for each user type.
2. For each user, select the article with the highest UCB score based on their type.
