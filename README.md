# Vaccinations:How past trends can help us improve current vaccination rates

**Authors**: Adonis McQueen, Emiko Naomasa, Julian Ward

## Objectives 

The objectives of this project are twofold. (1) Develop two prediction models to predict individual vaccination uptake’s for the seasonal flu vaccine and H1N1 flu vaccine using vaccination status survey data on the 2009 N1H1 flu and seasonal flu.
 (2) Given the developed prediction model, analyze socio-economic features strongly related to a person’s vaccination decision. 

## Business Problems

[For FY 2022, the US government has approved the most significant budget increase for the CDC in nearly two decades](https://www.cdc.gov/media/releases/2021/s0528-fiscal-year-2022.html). The budget is targeted to fund priority public health issues in the US, including improving readiness for future public health crises and reducing health disparities in racial and ethnic minority communities. 

To support their policymaking, the CDC has tasked us to create a vaccination prediction model to prepare for a future pandemic crisis. The CDC also asked us to provide policy recommendations based on the model. Remarkably, they are interested in which racial and ethnic communities to target, the critical factors for their vaccination decisions, and how to address barriers. 

## Data

Our dataset is from [DRIVENDATA](https://www.drivendata.org/competitions/66/flu-shot-learning/). This is a subsample of [the National 2009 H1N1 Flu Survey (NHFS)](https://www.cdc.gov/nchs/nis/data_files_h1n1.htm), which the CDC conducted from 2009 to 2010. Data cover the H1N1 and seasonal flu vaccination status of adults as well as flu-related behaviors, opinions about flu vaccine safety and effectiveness, and socioeconomic status as follows. 

•	**Knowledge and berief on influenza and vaccine:** Questions on concern, knowledge and opinion on H1N1/seasonal influenza and vaccine  
•	**Attitude toward influenza preventive measures:** Behavioral questions on avoidance of large gathering, wearing face mask, washing hands, touching face   
•	**Socioeconomic factors:** Age group, Income group, Education, Race, Sex, Marital status, Employment status, Urban/Rural, Home ownership, Number of people live together\
•	**Health consideration factors:** High risk group, Doctor's recommendations, Health Insurance 

After clearning, our data includes 35 vaccination features. 


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

Compared to the benchmark (not Baseline!) model provided by the data source.

******************************
| H1N1        | Score       | Seasonal    | Score       |
| ----------- | ----------- | ----------- | ----------- |
| Precision   | .67         | Precision   | .76         |
| Recall      | .43         | Recall      | .71         |
| F1          | .52         | F1          | .74         |
| Accuracy    | .83         | Accuracy    | .76         |
| ROC-AUC     | .8278       | ROC-AUC     | .8311       |

We scored minor improvements across the board compared to the benchmark model.

## Results

Our model provided a number of insights, expecially in the analysis of feature importance. 

**Insert Image Here**

In both our models having a doctor's direct intervention was the most important factor in determining outcome. Additionally, concerns about both the efficacy of the vaccine and concerns about the danger of the illness itself loom large. On the one hand this presents an opportunity for our stakeholders to address. On the other hand, it points to where current policy is failing our communities of concern. 

Additionally, it is important to note the importance that opinions about seasonal vaccinations  rank in the top ten most important features even for H1N1 vaccine uptake. This indicates that under pandemic or emergency conditions it is important to have an underlying base of trust and knowledge regarding vaccination in general. 

Notably, despite the racial disparities evident in the data, these factors are not seen as highly predictive in our model *given the other factors present*. That is, many disparities in outcomes for racial minorities can be explained in the model by disparities in, e.g. access to doctors, health insurance, or information about vaccines. We can see this with a simple breakdown by race of who has recieved recommendations for the seasonal flu vaccine. Almost half of all White respondents had recieved a recommendation from their doctor, while just over a third of Black respondents had. 

## Policy Recommendations 

- Target vaccination outreach to communities with certain ethnicities. 
- Address concerns about vaccine efficacy and safety. 
- Given the critical importance of doctor's recomendations to vaccine uptake, all efforts should be made to expand access to medical professionals in underserved communities, and measures be taken to 



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
