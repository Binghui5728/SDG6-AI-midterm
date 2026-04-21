# SDG6-AI-midterm
資安博三112C72103 林秉輝 Personal Midterm Report:：
Propose a Machine Learning (ML)-based solution to address a Sustainable Development Goal (SDG) challenge, including the following aspects:

1.Clear Problem Definition – Clearly define the SDG-related problem you aim to solve.
•	Alignment with Sustainable Development Goals (SDGs)
  o	SDG 6.1: Achieve universal and equitable access to safe and affordable drinking water for all.
  o	SDG 6.3: Improve water quality by reducing pollution.
•	Problem Description：Traditional water quality testing relies heavily on manual sampling and laboratory analysis, which is both time-consuming and incapable of providing real-time early warnings. Consequently, if a water source experiences sudden contamination, the delay in detection poses a significant threat to community health.
•	Project Objective：To leverage machine learning to analyze multidimensional water quality indicators (e.g., pH levels, hardness, chlorine content, etc.) and automatically determine the potability of water samples, thereby achieving low-cost, real-time monitoring.

2.Data Sources and Processing – Describe the data sources and how the data is processed. 
[Include a sample code snippet for data processing]
[update for next year: Specify the Referenced Kaggle project and the Gemini Colab interaction progressas another attachment ]
•	Reference Dataset: https://www.kaggle.com/datasets/adityakadiwal/water-potability
•	code snippet for data processing（Gemini Colab）： https://colab.research.google.com/drive/1zhMp_LrNAAwyKyA9z8Cg7TKc3ZGohRQ4?usp=sharing
•	Key Features:
  o	pH Level: Acidity or alkalinity.
  o	Turbidity: Level of suspended solids.
  o	Chloramines: Residual disinfectant levels.
  o	Conductivity: Concentration of dissolved salts in water.
•	Key Processing Focus:
  o	Handling Missing Data: The dataset often has missing pH values, requiring imputation using mean or median values.
  o	Feature Scaling: Due to significant differences in units across metrics (e.g., conductivity vs. pH), normalization is required.
  
3.Model Selection and Discussion – Explain the ML model used and discuss its suitability.
•	Proposed Models: Support Vector Machines (SVM) or Random Forest
•	Discussion:
  o	Non-linear Relationships: Water potability is generally not determined by a single indicator, but rather by a non-linear combination of multiple features. SVM, paired with an RBF (Radial Basis Function) Kernel, is highly effective at managing these types of high-dimensional classification problems.
  o	Reliability: Random Forest excels at handling outliers within the dataset. Furthermore, it provides feature importance ranking, which enables us to determine which indicators have the most significant impact on water quality.

4.Training and Testing – Describe the training and testing process. [Preliminary results are preferred]
