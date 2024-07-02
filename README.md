# YouTube Sentiment Analysis System

This repository contains the code and documentation for the YouTube Sentiment Analysis System. The system is designed to collect and analyze comments from YouTube videos using sentiment analysis techniques to provide valuable insights for researchers and content creators.

## Table of Contents
- [Introduction](#introduction)
- [Methodology](#methodology)
  - [Finding the Best Pre-Trained Model](#finding-the-best-pre-trained-model)
  - [Collecting YouTube Video Comments](#collecting-youtube-video-comments)
  - [Analyzing Comment Topics](#analyzing-comment-topics)
- [Results and Discussion](#results-and-discussion)
  - [Model Performance](#model-performance)
  - [Sentiment Analysis](#sentiment-analysis)
- [Limitations and Future Directions](#limitations-and-future-directions)
- [Conclusion](#conclusion)

## Introduction

Social media platforms, especially YouTube, generate vast amounts of user comments that are valuable for understanding audience feedback and engagement. Manually analyzing these comments is impractical due to their volume. Our system automates this process by collecting comments from YouTube videos and performing sentiment analysis to determine overall viewer sentiment and key discussion topics.

## Methodology

### Finding the Best Pre-Trained Model

We evaluated two pre-trained models for sentiment analysis: BERT and RoBERTa. Using the 'Twitter Sentiment Analysis' dataset from Kaggle, we fine-tuned these models and compared their performance based on accuracy, precision, recall, and F1 score. RoBERTa was selected for its superior performance in distinguishing positive and negative sentiments.

### Collecting YouTube Video Comments

We utilized the YouTube Data API v3 to collect comments from YouTube videos. This API allows for efficient extraction of comments, bypassing the need for web scraping.

### Analyzing Comment Topics

To understand the topics discussed in the comment section, we counted the occurrences of each unique word, excluding common stopwords. This data was visualized using word clouds, highlighting the most frequently mentioned terms.

## Results and Discussion

### Model Performance

| Model   | Accuracy | Precision | Recall | F1 Score |
|---------|----------|-----------|--------|----------|
| BERT    | 87.07%   | 0.86      | 0.87   | 0.86     |
| RoBERTa | 85.71%   | 0.83      | 0.86   | 0.83     |

RoBERTa was chosen for further analysis due to its ability to accurately predict positive and negative sentiments, which are crucial for practical applications.

### Sentiment Analysis

Applying the RoBERTa model to YouTube comments provided detailed insights into viewer feedback. For example, analysis of PewDiePie's video "How a Reddit Post Changed my Life" showed 73.5% positive sentiments, while Logan Paul's controversial video resulted in 75.94% negative sentiments. Such insights help content creators improve viewer satisfaction and engagement.

## Limitations and Future Directions

Our system faced limitations due to hardware constraints and API usage limits. Future improvements could include further fine-tuning of the sentiment analysis model, expanding analysis to other social media platforms, and integrating text summarization features to better understand audience views.

## Conclusion

This project demonstrates the potential of automated sentiment analysis in providing valuable insights into audience feedback on social media platforms. By leveraging pre-trained models and API integrations, we can transform the manual process of sentiment analysis into an efficient, automated system.

