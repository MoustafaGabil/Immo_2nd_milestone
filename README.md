# Data Analysis

- Repository: `immo-eliza-teamname-analysis` 
- Type: `Learning and consolidation`
- Duration: `5 days`
- Deadline: 22/10/2024 12:30 PM (code + presentations)
- Team: team (3-4 people)

## Mission Objectives

- Be able to use `pandas`
- Be able to use a data visualization library of your choice (such as `matplotlib`, `seaborn`, or `plotly)
- Be able to clean a dataset for analysis
- Be able to use colors in visualizations correctly
- Be able to establish conclusions about a dataset
- Be able to find and answer creative questions about data
- Be able to present your insights to a non-technical audience
- Be able to work in a group project

## The Mission

The real estate company Immo Eliza wants to establish itself as the biggest Belgian real estate services provider. To achieve that goal, they need to more accurately and faster than their competitors estimate the value of properties, to pick out those properties that are most valuable to them and their clients.

Enter creating a machine learning model to predict the prices of properties across Belgium. Having no in-house data scientists, they are looking for talented people to do it for them. Since your last encounter with them went great, they continue to rely on you to do the job. Everything is in your hands now!

By the end of this week, Immo Eliza's management wants to see a preliminary analysis based on the dataset you previously scraped. The management has no technical background. Broadly speaking, they have two main questions: 
- What are currently the most interesting insights about the Belgian real estate market?
- What variables are the most important when determining the price of a property?

## Steps

### Step 0: Team Organization

Each team will be assing a team leader and a repo manager. Here are their responsibilities:

- Team leader: Is the main point of contant of the coach. They will lead the teams daily discussions on how to tackle the project and keep track of team members progress.
- Repo manager: They are the only person allowed to merge to the main branch. 
- Developers: Everyone! You will all work on tackling the problem.

**Important:**  To help with the project management, each team will have a Trello board keeping track of their tasks and their progress. Each team leader will invite the coach. Each person on the team should work in their own branch!

### Step 1: Data Cleaning

You have collected your data, time to further clean it.

A cleaned dataset is a dataset that doesn't contain any duplicates, has no blank spaces, and has no other obvious errors. The rest of the analysis is worthless if you neglect this step; Garbage In, Garbage Out.

Take care of the following:
- No duplicates
- No blank spaces (e.g. `" I love python "` => `"I love python"`)
- No empty values (set them to `None` or `NaN`)
- No wrongly encoded values (e.g. a text value in the price column)

# Extra's
- Locality clean-up (lower-characters?) 
- No blank spaces (e.g. `" I love python "` => `"I love python"`)
- No empty values (set them to `None` or `NaN`)


### Step 2: Data Analysis

Now that the data has been both collected and cleaned, let's move on to the analysis.

You **must** be able to answer following questions (with a vizualization if appropriate):
1. How many observations and features do you have?
2. What is the proportion of missing values per column?
3. Which variables would you delete and why?
4. What variables are most subject to outliers?
5. How many qualitative and quantitative variables are there? How would you transform the qualitative values into numerical values?
6. What is the correlation between the variables and the price? Why do you think some variables are more correlated than others?
7. How are the variables themselves correlated to each other? Can you find groups of variables that are correlated together?
8. How are the number of properties distributed according to their surface?
9. Which five variables do you consider the most important and why?
10. What are the least/most expensive municipalities in Belgium/Wallonia/Flanders? (_in terms of price per m², average price, and median price_)

This is a non-exhaustive list of possible questions. Try to make a maximum number of interpretations from the dataset. **Bonus points for creative and out-of-the-box insights.**

1. Plots per subtype (house/appartment/villa/...)

2. 

Use tools such as `matplotlib`, `seaborn`, `plotly`, or [insert whatever visualization tool you find useful]...

> Do your analysis in notebooks. No real need for scripting in this case, you'll want to have your hands free to experiment and explore the data in many directions. Writing functions for code you reuse is still a good idea, don't lose track of your good habits. Don't make it too messy though, your results should be reproducible and Immo Eliza's CEO might ask to rerun an analysis with a slight change :-)

### Step 3: Presentation

After analyzing your data, you're finally ready to present your results. You have to communicate your analysis using simple words and clear graphs, and ideally also deliver a few recommendations.

You can make your **plots** presentation-ready by accounting for the following points:
- A clear title
- A legend (if applicable)
- Add axis labels (in understandable language, no variable names)
- Add axis units
- Have comparable scales
- Have no overlapping text
- A main takeaway
- Remove all clutter that doesn't contribute to the message
- Smart use of [colors](https://chartio.com/learn/charts/how-to-choose-colors-data-visualization/)

> Don't mention data cleaning in your presentation as this is a technical background task. You should focus on the insights you found and the recommendations you can make.

## Repository

Create a new repository for the analysis and modeling steps of the project.

Establish the following:
- In your `data/` folder
   - Have a `raw/` folder with the original dataset
   - Have a `cleaned/` folder with the cleaned dataset
- Make a `clean.py` script for any additional cleaning
- Add your notebooks in an `analysis/`cleaning_data_urson cleaning_data_majid folder
- Put your finalized presentation in `.pdf` format in a `reports/` folder

In general, **think modular**! You do not want to run all steps at once, so your code should be tailored to that gradual process: scrape, clean, analyze, model, deploy, ...

## Deliverables

As main deliverable, we expect a compelling presentation of **10 minutes + 5 minutes Q&A** that conveys your data analysis including at least five well-crafted visualizations. Use Canva for your presentations and incorporate the feedback from your previous presentation.

Next to that, your repository should be updated.

On **Tuesday 22/10** in the afternoon,you present your presentation to your coach(es) and collagues. They will give you feedback on the content and the structure.

## Evaluation criteria

| Criteria       | Indicator                                            | Yes/No |
-----------------|------------------------------------------------------| ------ |
| 1. Is complete | Know how to answer all the above questions           |        |
|                | Good use of `pandas` and a visualization library     |        |
|                | Deliver a convincing presentation                    |        |
|                | Clean notebook(s)                                    |        |
|                | An updated repository                                |        |
| 2. Is great    | Creative questions were answered                     |        |
|                | The colors are chosen carefully                      |        |

## Quotes

_"The lottery is a tax on people who don't understand statistics." - Anonymous_

![You've got this!](https://media.giphy.com/media/JrXas5ecb4FkwbFpIE/giphy.gif)