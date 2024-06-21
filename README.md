# Market of One - Identifying Characteristics of Online Profiles

This repository contains the code and data used in the MSc. Dissertation titled "Market of One: Identifying Characteristics of Online Profiles," presented to the School of Mathematics Sciences at the University of Southampton.

## Table of Contents

1. [Key Insights](#key-insights)
2. [Introduction](#introduction)
3. [Project Overview](#project-overview)
4. [Prerequisites](#prerequisites)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Data Preparation](#data-preparation)
8. [Extraction of Attributes](#extraction-of-attributes)
9. [Classification Analysis](#classification-analysis)
10. [Results and Findings](#results-and-findings)
11. [Conclusion](#conclusion)
12. [Acknowledgements](#acknowledgements)
13. [References](#references)

## Key Insights

- **Gender Classification**: Achieved an accuracy of 72.35% using Support Vector Machine (SVM), with notable indicators including specific keywords and username patterns.
- **Age Classification**: Utilized a combination of regular expressions and textual analysis to categorize users into age groups with a best accuracy of 68.85% using XGBoost.
- **Occupation Classification**: Leveraged keyword-based classification to accurately identify user occupations, achieving an accuracy of 68.35% with SVM.
- **Data Volume**: Analyzed a comprehensive dataset of 3.5 million Twitter users, distilled down to 118,640 cases after rigorous preprocessing and attribute extraction.
- **Methodology**: Implemented advanced machine learning techniques and natural language processing (NLP) to extract and classify demographic attributes from user-generated content.

## Introduction

The objective of this research is to identify demographic characteristics such as age, gender, and occupation of Twitter users through machine learning techniques. The methodology includes analyzing textual data from a comprehensive dataset of Twitter profiles and tweets.

## Project Overview

The project is divided into two main stages:
1. Extraction of demographic attributes from user bios and tweets.
2. Classification of textual content based on the identified attributes.

## Prerequisites

Before you begin, ensure you have met the following requirements:
- Python 3.x
- Libraries: pandas, numpy, scikit-learn, nltk, regex, langdetect

## Installation

1. Clone this repository:
    ```bash
    git clone https://github.com/Ashish-Johnson/market-of-one.git
    cd market-of-one
    ```

2. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Data Preparation**:
    - Clean and preprocess the raw data by removing non-English entries, special characters, and duplicates.
    - Feature selection includes retaining relevant columns such as `user_description` and `tweets`.

2. **Extraction of Attributes**:
    - Gender Extraction: Based on usernames and specific keywords from user descriptions.
    - Age Extraction: Using regular expressions and textual analysis to identify age-related patterns.
    - Occupation Extraction: Utilizing a keyword-centric approach to categorize users into predefined occupational groups.

3. **Classification Analysis**:
    - Implement machine learning models (e.g., SVM, XGBoost) to classify gender, age, and occupation.
    - Evaluate the models using metrics like accuracy, precision, and recall.

## Data Preparation

The data preparation phase involves several steps:
- Removing non-English entries using the `langdetect` library.
- Cleaning the dataset by removing special characters and hyperlinks.
- Eliminating stop words and standardizing text case.

## Extraction of Attributes

### Gender Extraction
- Implemented using the `gender_guesser` library based on first names.
- Analyzed specific keywords in user descriptions to determine gender.

### Age Extraction
- Employed regular expressions to identify age-related information.
- Used textual hints and keywords to categorize age into defined groups.

### Occupation Extraction
- Developed a keyword-based function to classify occupations.
- Refined initial categories into a more focused set for better accuracy.

## Classification Analysis

The classification analysis includes:
- Transforming textual data using TF-IDF.
- Building and evaluating models like SVM, XGBoost, Logistic Regression.
- Addressing potential biases and refining model parameters.

## Results and Findings

The study achieved notable accuracy in classifying demographic attributes:
- Gender classification accuracy: 72.35% (SVM)
- Age classification accuracy: 68.85% (XGBoost)
- Occupation classification accuracy: 68.35% (SVM)

## Conclusion

The research demonstrates the capability of machine learning techniques in identifying demographic characteristics from online profiles. Continuous improvement and careful implementation are essential to ensure reliable results in diverse social media contexts.

## Acknowledgements

I extend my deepest gratitude to my academic supervisor, Voung Phan, and industrial supervisor, Dimitri Lesas, for their guidance and support. Special thanks to my personal academic tutor, Selin Ahipasaoglu, and our industry partner, Roke, for their invaluable contributions.

