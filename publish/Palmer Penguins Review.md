---
title: "Palmer Penguins Review"
excerpt: "A Predictive Model Approach"
date: "2024-8-1"
author:
    name: "Alec Brooks"
    url: "https://media.licdn.com/dms/image/D5603AQG0j7-Cwz80BA/profile-displayphoto-shrink_800_800/0/1721083708589?e=1727913600&v=beta&t=hRKFU6mFBKX4S_RwKkbd0H1cx99B3K3xvpffLoFbd4I"
ogImage:
    url: "https://blog.abrooks.dev/md_assets/attachments/Pasted%20image%2020240802124444.png"
---
# Palmer Penguins Review: a Predictive Model Approach

![[Pasted image 20240802124444.png]]
## Abstract
The Palmer Penguin dataset is widely used in academic settings due to its variety and scope, making it a good tool for exploring different types of statistical analysis. The dataset includes seven different metrics that can be analyzed for various insights. This report focuses on the correlation between penguin Body Mass and Flipper Length. This analysis shows that Flipper Length can be used as a reliable predictor of penguin Body Mass, using the formula 𝑦 = 50.153𝑥 − 5872.1 within acceptable levels of accuracy. However, these findings are preliminary, and further analysis could reveal an additional wealth of other connections within the dataset.
## Data Set
In this report, we will be examining the "palmer-penguins" dataset, provided by Allison Horst, a data scientist and artist on GitHub. The data was collected from 07 - 09 by Dr. Kristen Gorman, while working with the US Long Term Ecological Research Network. This dataset includes three categorical variables. species, island, and sex, along with four numerical variables. culmen_length_mm, culmen_depth_mm, flipper_length_mm, and body_mass_g. Together, these variables form the palmer-penguins dataset, which is largely used in training and classroom settings due to its simplicity and variety of variable types.
## Data Exploration
Upon initial exploration of our dataset, we observe that all present numerical variables appear to be consistent with relatively low deviation.
![[Pasted image 20240802125301.png]]
As always, this exploration includes examining missing values. By doing this, we uncover three important facts that may be relevant to our analysis:

1. The dataset includes 344 total rows.
2. The "sex" variable has one missing value and 10 NAs.
3. Two records in our dataset include species and island values but are missing all numerical data.

![](file:///C:/Users/ALECDE~1.001/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)
![](file:///C:/Users/ALECDE~1.001/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

These inconsistencies may become relevant in our analysis and will need to be addressed.
# Data Preparation
To begin with data preparation, we removed rows containing NAs and numerically encoded the categorical variables, which grants more flexibility in our analysis.
![[Pasted image 20240802125500.png]]

![[Pasted image 20240802125658.png]]

One benefit of this encoding is that it makes it much easier to build a correlation matrix.  

![[Pasted image 20240802125758.png]]
# Preliminary Analysis
![[Pasted image 20240802125854.png]]
If we take a look at each quartile of our measurement variables it reveals a significant range and variability, with body mass showing the highest variation. Flipper length and body mass display moderate variability, making them suitable predictors for a linear regression model.
![[Pasted image 20240802131553.png]]
## Analysis
If we plot Flipper Length as our independent variable and Body Mass as our dependent variable, we can see a consistent pattern. The R² score of 0.76 indicates that approximately 76% of the variance in Body Mass can be explained by Flipper Length. After we plot the residuals, we find a relatively low Mean Residual of 0.06.

![](file:///C:/Users/ALECDE~1.001/AppData/Local/Temp/msohtmlclip1/01/clip_image024.jpg)

![](file:///C:/Users/ALECDE~1.001/AppData/Local/Temp/msohtmlclip1/01/clip_image026.jpg)
# Conclusion
Further, The Standard Error is 393.34. Considering that the range of the dependent variable (Body Mass) is 6300, this Standard Error is relatively low, representing about 6.24% of the Body Mass range. This indicates that the model is reasonably accurate, making Flipper Length an acceptable predictor of Body Mass. This project serves as a good case study for the importance of using methods such as plotting and analyzing residuals to verify findings.