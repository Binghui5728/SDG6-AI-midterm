# SDG6-AI-midterm
資安博三112C72103 林秉輝 Personal Midterm Report:：
Propose a Machine Learning (ML)-based solution to address a Sustainable Development Goal (SDG) challenge, including the following aspects:

1.Clear Problem Definition – Clearly define the SDG-related problem you aim to solve.
•	對應目標： SDG 6.1（人人都能享有安全且負擔得起的飲用水）及 6.3（減少污染、提高水質）。
•	問題描述： 傳統的水質檢測依賴人工採樣與實驗室分析，耗時且無法做到即時預警。當水源受到突發性污染（如工業排放或極端氣候導致的濁度增加）時，延遲發現會對社區健康造成威脅。
•	目標： 利用機器學習分析水質的多維度指標（如 pH 值、硬度、氯含量等），自動判斷水樣是否安全可飲用 (Potability)，實現低成本的即時監測。

2.Data Sources and Processing – Describe the data sources and how the data is processed. 
[Include a sample code snippet for data processing]
[update for next year: Specify the Referenced Kaggle project and the Gemini Colab interaction progressas another attachment ]
•	參考數據集： https://www.kaggle.com/datasets/adityakadiwal/water-potability
•	code snippet for data processing（Gemini Colab）： https://colab.research.google.com/drive/1zhMp_LrNAAwyKyA9z8Cg7TKc3ZGohRQ4?usp=sharing
•	關鍵特徵：
  o	pH 值： 酸鹼度。
  o	Turbidity (濁度)： 懸浮物含量。
  o	Chloramines (氯胺)： 消毒劑殘留量。
  o	Conductivity (電導率)： 水中溶解鹽類濃度。
•	處理重點：
  o	缺失值補全： 該數據集常有 pH 值缺失，需使用均值或中位數填充。
  o	特徵縮放： 不同指標單位差異巨大（如電導率與 pH 值），需進行歸一化。

3.Model Selection and Discussion – Explain the ML model used and discuss its suitability.
•	擬選用模型：Support Vector Machines (SVM) 或 Random Forest
•	討論：
  o	非線性關係：水質是否可飲用通常不是單一指標決定的，而是多個特徵間的非線性組合。SVM 搭配 RBF Kernel 能有效處理這類高維度的分類問題。
  o	可靠性： 隨機森林則能處理數據中的異常值（Outliers），並提供特徵重要性排序，讓我們知道哪個指標對水質影響最大。

4.Training and Testing – Describe the training and testing process. [Preliminary results are preferred]
