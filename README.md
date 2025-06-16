# The Economics of Film: An Investigation of the Financial Interplay Between Film Releases and Stock Market Trends

## Group Members

Member-1: Lizzie Healy\
Member-2: Sophia Rutman\
Member-3: Amina Nsanza\
Member-4: Rachna Rawalpally

## Purpose

The purpose of this project was to investigate the bidirectional relationship between the state of the economy and the film industry. Specifically, we set out to achieve two distinct goals:
  1. **Films impacting stocks**: Analyze how film releases impact stock market closing values.
  2. **Stocks impacting films**: Analyze how economic conditions influence film revenues.

We utilized the stock market closing values, particularly, the S&P index to proxy for the overall strength of the economy and box office values to measure film success. We hypothesized that an underlying relationship exists between the film industry and stock market movement, and that relationship is observable through statistical analysis.

Data for stock market performance was collected from a Professor at Bowdoin College who utilized publicly available financial sources, while film-related data was scraped utilizing IMDb's OMDB API. Our analysis involved feature selection following by regression modeling for both of our objectives.

## Setup Instructions

This work was mainly for purposes of creating a poster presentation and written report and is recommended to absorb this code in the viewing sense (.html files are also included). Nonetheless, the code is available for reproduction purposes. This is achievable through:
  1. Cloning this Repository to your local machine
  2. Installing the Required packages
  3. Collecting the stock data from perferred source (reaching out to the authors for the data or through a publicly available site such as yahoofinance.com)
  4. Collecting the IMBd movie data utilizing the OMDB scraping file found in data/datacollect.ipynb
  5. If looking to perform feature selection (navigate to the feature_selection folder):\
    a. Run the feature_selection_films.ipynb\
    b. Run the feature_selection_stocks.ipynb
  6. If looking to perform modeling (navigate to the modeling file):\
    c. Run the modeling-stock-to-bo.ipynb\
    d. Run polynom_predicting_bo.qmd\
    e. Run newmoviemodel.ipynb

## Usage Examples

While we do not claim that this research will enable accurate stock market predictions or guarentee success in the film industry, we do belive it represents a meaningful step toward understanding a small segment of the economy. Our findings could help:
  1. Film producers better assess which types of films are likely to be perform well based on the current economic conditions and general sentiment of the nation.
  2. Financial analyst might incorporate film releases as part of their broader workflow when analyzing stock market movement and trends.
  3. Economic Researchers attempting to study the intersection of culture and economics.

## Project Structure
- /data/: contains the code to obtain movie features by scraping IMDb
- /feature_selection/: contains film and stock feature selection code files and rendered versions
- /modeling/: contains regression code files and rendered versions
- /prev_repo_commit_history/: previous commit history from earlier github repository
- merge.ipynb: file containing code for combining the film and stock datasets
- /README: project overview
- /ACF.ipynb: contains code investigating autocorrelation

## Abstract

This paper investigates the financial interplay between the film industry and the stock market, examining how movie releases may influence market trends and vice versa. Using a dataset combining stock performance data from major S&P 500 corporations and movie characteristics scraped from IMDb via the OMDb API; we conducted regression analyses, feature selection, and predictive modeling to explore these relationships. We evaluated both directions of influence: how stock trends relate to box office revenues and whether movie features can predict stock market movements. While binary classification models such as logistic regression and SVM performed poorly, suggesting that movie features alone cannot predict stock movements, more complex models like XGBoost captured some nonlinear patterns, achieving an R² of 0.76 when predicting stock changes based on selected features. Overall, the study highlights a limited connection between economic indicators and film success, suggesting avenues for future research using more advanced time-dependent models.
