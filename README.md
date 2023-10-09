
# xG Modeling

**Author**: Lucas Kimball

![img](https://github.com/LMK08/xG_Project/blob/main/Images/download-3.jpg)

## What are Expected Goals (xG)?

Expected Goals (xG) is a statistical metric used in soccer (football) to quantify the quality and likelihood of a scoring opportunity during a match. It's a way to assess the probability that a shot will result in a goal based on various factors and historical data.

Here's a breakdown of how xG is calculated and what it represents:

Shot Characteristics: xG takes into account various parameters of a shot, including:

- Distance from the goal
- Angle of the shot
- Type of play (e.g., open play, set piece, counterattack)
- bodypart used to shoot
  
Historical Data: Analysts and data scientists use large datasets from past matches to analyze how likely shots with similar characteristics were to result in goals.

Probability Assignment: For each shot, a probability of it resulting in a goal is assigned based on the historical data. This probability ranges from 0 to 1, where a value approaching 0 means the shot is unlikely to be a goal and a value approaching 1 means it's highly likely.

xG is a valuable tool for coaches, analysts, and fans to analyze a team's performance, beyond just looking at the scoreline. It helps in identifying how well a team created and converted scoring opportunities during a match or across a series of matches, and it's often used for tactical analysis and scouting.

##  Overview

For this project, I build a Logistic Regression model using shot data from soccer matches. Through the deployment of this model, our aim is to offer a  insights to Premier League soccer team AFC Richmond.

### Business Problem

The Premier League Football team AFC Richmond has hired consulting data scientists to analyze their past season in which they barely avoided relegation. Using historical data, the data scientists are tasked with providing insights that will improve tactics, information on the strength of AFC Richmonds attack and defense, and advice to their player recruitment team.


## Data

- from [Statsbomb's](https://github.com/statsbomb/open-data) database
- Data is from the 2020 Euros, 2020-21 La Liga season, 2022 World Cup
- 3348 shots in total


## Process

- Isolated all competitions in the dataset that had 360 data available
- Selected the 3 men's competitions (only 2 available for women's competions)
- Calculated Angle and Distance for all shots based on their X,Y coordinates
- Created baseline logistic regression model
- Attempted different parameter tuning to optimize the AUC ROC curve including L1 and L2 penalties, threshold optimization, and C-value optimization



## Visuals

Shot Map
![img](https://github.com/LMK08/xG_Project/blob/main/Images/Screenshot%202023-10-09%20at%2012.14.37%20AM.png)

Goal Map
![img](https://github.com/LMK08/xG_Project/blob/main/Images/Screenshot%202023-10-09%20at%2012.14.47%20AM.png)

Goal Probability Map
![img](https://github.com/LMK08/xG_Project/blob/main/Images/Screenshot%202023-10-09%20at%2012.14.55%20AM.png)

Logistic Regression Model
![img](https://github.com/LMK08/xG_Project/blob/main/Images/Screenshot%202023-10-09%20at%2012.02.46%20AM.png)

Model Coeffcients for each feature
![img](https://github.com/LMK08/xG_Project/blob/main/Images/Screenshot%202023-10-06%20at%209.21.42%20AM.png)



### Next Steps

- Use model on larger dataset to find specific players to recommend 

- Develop model to determine value of non-goalscorers (ie. xThreat, Goal Probability added)

- Incorporate features such as defender and goalkeeper positioning
- 

## For More Information

Please review the full analysis in [my Jupyter Notebook](./JupyterNotebookFinal) or my [presentation](./xG_Model_Presentation).


For any additional questions, please contact:

Lucas Kimball & lucaskimball98@gmail.com**



## Repository Structure

```
├── images

├── JupyterNotebookFinal.ipynb
├── README.md
├── .gitignore
├── xG_Model_Presentation.pdf
└── JupyterNotebookFinal.pdf
```
