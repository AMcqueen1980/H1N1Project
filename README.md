# Vaccinations:How past trends can help us improve current vaccination rates

**Authors**: Adonis McQueen, Emiko Naomasa, Julian Ward

## Objectives 

The largest global vaccination campaign in history is currently underway. In the United States, mass vaccinations began in December 2020, and about 60% have completed their second doses as of November 2021. For fast and effective vaccination rollout, the Centers for Disease Control and Prevention (CDC) closely monitors and predicts vaccination coverage across the country. In this project, to contribute to the CDC’s vaccination monitoring efforts, we develop a machine learning model to predict an individual’s vaccination uptake for the time of the pandemic as well as for regular seasonal flu using vaccination status survey data on 2009 N1H1 flu and seasonal flu.

Our model will help the CDC to quickly assess who will be vaccinated and who will not across different socio-economic and demographic groups. Our model also includes data on a person’s knowledge, concerns, and beliefs about the vaccine and the flu; thus, our model will address major challenges for improving vaccination uptake. Finally, from our model and data analysis, we will suggest policy recommendations for which communities to target in a vaccination campaign, and how to address people’s concerns about vaccinations. Our analysis and recommendations will support CDC’s vaccination effort to combat the current pandemic and flu season. 

## Vaccination Challenges

It is widely reported that vaccination rates are disproportionately low among African Americans, Hispanics, and other ethnic minority groups. There are many reasons for these differences, including access to health insurance, physical access to a vaccination facility, knowledge gaps, attitudes towards vaccination, or lack of trust in health providers. Our model includes various variables representing major barriers to vaccination uptakes, including a person’s beliefs about vaccines, knowledge of influenza and vaccines, and other socioeconomic factors, and aims to provide evidence-based policy recommendations to CDC on what the major barriers to vaccination are and how to address these gaps. 

## Data

Our dataset is from [DRIVENDATA](https://www.drivendata.org/competitions/66/flu-shot-learning/). This is a subsample of [the National 2009 H1N1 Flu Survey (NHFS)](https://www.cdc.gov/nchs/nis/data_files_h1n1.htm), which the CDC conducted from 2009 to 2010. Data cover the H1N1 and seasonal flu vaccination status of adults as well as flu-related behaviors, opinions about flu vaccine safety and effectiveness, and socioeconomic status as follows. 

•	**Knowledge and berief on influenza and vaccine:** Questions on concern, knowledge and opinion on H1N1/seasonal influenza and vaccine  
•	**Attitude toward influenza preventive measures:** Behavioral questions on avoidance of large gathering, wearing face mask, washing hands, touching face   
•	**Socioeconomic factors:** Age group, Income group, Education, Race, Sex, Marital status, Employment status, Urban/Rural, Home ownership, Number of people live together\
•	**Health consideration factors:** High risk group, Doctor's recommendations, Health Insurance 

After clearning, our data includes 35 vaccination features for XXXX individuals

- Add summary stat


## Model and Metrics

We ultimately chose to use two seperate models for our two targets. Both are Gradient Boosting Classifier models with parameters optimised via GridSearch, however they each been fit with a different model in mind. 

The metrics for our final H1N1 model is:

******************************
| Got Vaccinated  | Score       |
| -----------     | ----------- |
| Precision       | .69         |
| Recall          | .45         |
| F1              | .55         |
| Accuracy        | .84         |
| ROC-AUC         | .8364       |

And for our final Seasonal Flu model: 

******************************
| Got Vaccinated  | Score       |
| -----------     | ----------- |
| Precision       | .77         |
| Recall          | .75         |
| F1              | .76         |
| Accuracy        | .78         |
| ROC-AUC         | .8536       |

Compared to the Benchmark (Not Baseline!) model provided

******************************
| H1N1        | Score       | Seasonal    | Score       |
| ----------- | ----------- | ----------- | ----------- |
| Precision   | .67         | Precision   | .76         |
| Recall      | .43         | Recall      | .71         |
| F1          | .52         | F1          | .74         |
| Accuracy    | .83         | Accuracy    | .76         |
| ROC-AUC     | .8278       | ROC-AUC     | .8311       |


## Results

## Policy Recommendations 

- Target vaccination outreach to communities with certain ethnicities. 
- Address concerns about vaccine efficacy and safety. 

## Conclusions

## For More Information

Please review our full analysis in our Jupyter Notebook (<- insert link). 

For any additional questions, please contact Adonis McQueen, [Emiko Naomasa](emikonaomasa@gmail.com), Julian Ward

## Repository Structure

```
├── README.md                           <- The top-level README for reviewers of this project
├── Notebook.ipynb                      <- Full analysis in Jupyter notebook
├── PPTs.pdf                            <- PDF version of project presentation
├── Data                                <- Both sourced externally and generated from code
└── Images (if any)                     <- Both sourced externally and generated from code
```
