---
title: "Finacial Article Categoriser"
date: 2018-12-02
tags: [machine learning, data science]
header:
  image: "/images/finance/categorizer.png"
excerpt: "Natural Language Processing, Data Science"
mathjax: "true"
---

### Introduction
This was my first data science project working with a client. The client is a company that specialises in financial products comparison like home loans, credit cards, superannuation etc.  To spread awareness of the various products managed by them, they place the products on websites that show mostly articles like new, blogs etc.

My objective here was to develop a model that will be able to read an article to automatically label which financial product was the closest to place near/next to a article.

<img src="{{ site.url }}{{ site.baseurl }}/images/finance/model-work.png" alt="linearly separable data">

### Project Workflow

<img src="{{ site.url }}{{ site.baseurl }}/images/finance/project-worflow.png" alt="linearly separable data">

### The Dataset
The client has been publishing their own financial articles which they have already labelled appropriately based on the context and collected. I was given access to this dataset via API. I wrote a code in python to pull all the labelled articles into my local system.
There were 8 required categories:

1.	Home-Loans
2.	Personal-Loans
3.	Car-Loans
4.	Credit Cards
5.	Superannuation
6.	Savings Accounts
7.	Term Deposits
8.	Bank Accounts

**Total articles: 2813**
<img src="{{ site.url }}{{ site.baseurl }}/images/finance/article-distribution.png" alt="linearly separable data">

Using this dataset, I will build a classifier that will learn from this dataset and predict the category on articles from external sources.

### Natural Language Processing
Since the data is text, I need to use Natural Language Processing (NLP). Simply put its a process that helps in conversion of text as we humans understand it into numerical representation that the machine learning model understands.
<img src="{{ site.url }}{{ site.baseurl }}/images/finance/nlp.png" alt="linearly separable data">

### Text Pre-processing/Cleaning
The above will find some numerical representation for every word. However, this won’t be useful as some words will appear commonly in all the categories and don’t contribute to the classification. I removed such words. Other steps followed to clean up the text,
* Removed contractions
* Removed numbers
* Removed junk words

The steps above will vary from project to project. I would try and fit a model for each cleaning step to check for improvement in performance.

### Exploring the Categories 
After the cleaning I looked at the top word, two-word combo in each category. Below is two-word combo bar plot for 4 of the categories
<img src="{{ site.url }}{{ site.baseurl }}/images/finance/words-bar.png" alt="linearly separable data">

## H2 Heading

### H3 Heading

Here's some basic text.

And here's some *italics*

Here's some **bold** text.

What about a [link](https://github.com/)?

Here's a bulleted list:
* First item
+ Second item
- Third item

Here's a numbered list:
1. First
2. Second
3. Third

Python code block:
```python
    import numpy as np

    def test_function(x, y):
      z = np.sum(x,y)
      return z
```

R code block:
```r
library(tidyverse)
df <- read_csv("some_file.csv")
head(df)
```

Here's some inline code `x+y`.

Here's an image:
<img src="{{ site.url }}{{ site.baseurl }}/images/finance/house.png" alt="linearly separable data">

Here's another image using Kramdown:
![alt]({{ site.url }}{{ site.baseurl }}/images/finance/house.png)

Here's some math:

$$z=x+y$$

You can also put it inline $$z=x+y$$