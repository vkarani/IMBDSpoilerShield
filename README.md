![https://github.com/vkarani/IMBDSpoilerShield/blob/main/Figs/Movie_reviewers.png](https://github.com/vkarani/IMBDSpoilerShield/blob/main/Figs/Movie_reviewers.png)

--------------------
# IMBDSpoilerShield

## What is it?
Avid theater goers provide plenty of reviews of movies that they have seen to sites like IMDB. The idea is to select those reviews that do not have spoilers and present these to visitors to the site to see if they would like to watch them.

## Table of Contents
 - [EDA](#eda)
 - [Text Preprocessing](#text-preprocessing)
 - [3 tower BERT transformer](#3-tower-BERT-transformer)
 - [Fully connected Neural Net](#fully-connected-neural-net)

## 🗂️ Repository Structure

```
Root/
├── Methods/            <- Code and notebooks
├── Docs/               <- pdf Reports
├── Figs/               <- Images 
```

## EDA
Starting with the original dataset, I check for imbalance and remove null data. We also check for word frequency distribution.

## Text Preprocessing
Here I balance classes and perform the test train split

## 3 tower BERT transformer
Here I separate the reviews, synopsis and summary columns and send them each through their own BERT transformer heads in order to get their embeddings

## Fully connected Neural Net
Here I combine the embeddings from the 3 towers and send them through a fully connected neural net to perform logistic regression for the is_spoiler decision.