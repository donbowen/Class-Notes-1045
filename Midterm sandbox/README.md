Data needed
    word list of positive tone
    word list of negative tone
    eliminate stop words 
    
Final sample... what will it look like?
- unit: is a firm at a point in time
- variables: 
    - date of 10-K filing
    - sentiment vars (10!)
    - return around 10-K date

Firm | Date (of filing) | sentiment score | returns
--- | --- | --- | --- 
A | 1-1-22 | 25% | 10%
B | 3-30-22 | 17% | -2%
C | 3-22-22 | 10% | -5%

Rough steps, we can refine/adjust later:
1. Pick the firms in the sample
1. Download the 10-K filings
1. Download the stock returns (how?)
1. Calculate sentiment scores
    - Better: % of + sentiment words in the 10-K
1. Make the analysis dataframe: Merge returns and sentiment scores 
1. EDA baby! Data cleaning... maybe reconstruct your sentiment scores or stock returns
1. Analysis
1. Write the report

Which prompts some questions (and my answers/our discussion)
1. Which firms?  ... S&P500... fine starting choice but could induce biases (lack of smaller firms)
1. Which filings/when? 10-K ... last one in calendar 2022
1. How to conduct the sentiment analysis to define the sentiment vars?

Repo structure:
- inputs/    with SP500, stock returns (?)
- 10K_files/ for the 10-K inputs
- .gitignore (10K_files, any bg data/folder)
- code files:
    - get_data
        - `pip install -U sec-edgar-downloader`
    - build_sample
    - ugly_analysis (free playground)
    - report

