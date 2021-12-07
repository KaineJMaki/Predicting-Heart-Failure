# **How you can predict heart failure before it happens.**

Project Group 28's exploration of heart-related issues.

>Gavin Bosman - github.com/gavinbos

>Thomas Chiarello - github.com/BoiledSpagett

>Kaine Makimoto - github.com/KaineJMaki

>Mekael Wasti - github.com/MekaelWasti

## **Introduction:**
Cardiovascular diseases are the leading cause of death globally, so it is extremely important to know what the warning signs are before it's too late. Our team analyzed clincal features for predicting heart disease events from a dataset provided by data scientist "fedesoriano" at Kaggle. 

fedesoriano. (September 2021). Heart Failure Prediction Dataset. Retrieved December 1 from https://www.kaggle.com/fedesoriano/heart-failure-prediction.

### **Description of Dataset:**
The data was collected through a combination of multiple datasets relating to the heart conditions. Five different heart datasets that had 11 related attributes were used. A total of 1190 observations were collected and compiled from various regions across the globe. From Cleveland, Ohio, to Switzerland, the combined dataset presents the largest available set of heart information.
  - Age - The age of the patient
  - Sex - The sex of the patient
  - ChestPainType - The patient's chest pain type: [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]  
  - RestingBP - The resting blood pressure of the patient (mm Hg)
  - Cholesterol - The serum cholesterol level (mm/dl)
  - FastingBS - The fasting blood sugar level (1: if FastingBS > 120 mg/dl, 0: otherwise)
  - RestingECG - The resting electrocardiogram results
  - MaxHR - The maximum heart rate achieved
  - ExerciseAngina - Exercise induced angina
  - Oldpeak - The oldpeak value
  - ST_Slope - The slope of the peak exercise ST segment
  - HeartDisease - Classifies if the patient has heart disease

## **Discussion:**
Through our thorough analysis of the dataset, we came to many different conclusions. The following is everything we concluded along with graphs and explanations of our results.

### **Chest pain severity:**

![TAGraph](https://user-images.githubusercontent.com/90229634/144931288-f3c20767-7ae7-4006-81d5-8d781fd134f3.png)

The above graph shows five attributes that can be determined to be below average, average, or above average among the patients. In this case, we are exploring the percentage of patients experiencing typical angina chest pain, and the attributes with above average levels. As we can see, almost 80% of patients with TA have a higher than normal resting blood pressure level. Following that, cholesterol levels appear high in almost 50% of TA patients, and almost half have diagnosed heart disease.

![ATAGraph](https://user-images.githubusercontent.com/90229634/144931436-73f70a6e-1462-4bb6-8927-738b0e52be71.png)

The above graph displays the same attributes as the previous but for patients with atypical angina chest pains. Both cholesterol and resting blood pressure levels are high among more than 50% of the patients with ATA. Already we are noticing that these two attributes may have some correlation with chest pains. The other three attributes appear in less than 15% of the patients.

![NAPGraph](https://user-images.githubusercontent.com/90229634/144931492-ed8ec320-3d2b-4cd0-ae1f-932223f216b2.png)

Next we have non-anginal chest pain. This one follows a trend more similar to the typical anginal chest pain, with more than 60% of patients experiencing high resting blood pressure. From this, it's interesting to note that typical anginal chest pain appears to be extremely similar in terms of health readings to non-anginal chest pain. We can conclude from this that the differnces between the two come from the physical feeling of the patient.

![ASYGraph](https://user-images.githubusercontent.com/90229634/144931547-8e33f6ff-e142-40d2-a008-6f4de5ea9fec.png)

Finally, asymptomatic patients surprisingly showcase the most concerning attributes. This is shocking as asymptomatic patients are not experiencing any symptoms. This is concerning as they may not even realize how much risk they have. Almost 80% of those with asymptomatic chest pains are diagnosed with heart disease, and over half of the patients have high readings overall.

In conclusion, those with asymptomatic chest pains are at the greatest risk. This means that patients suffering physcially from their chest pains may have it easier than those who are not. Patients shouldn't take their physical appearance and status as an indication of how their cardiovascular health is.

### **Can you still get heart disease with normal health attributes?**

With the information we have about each of the attributes, we have a rough idea on what is considered "normal." We want to find what percentage of people with heart disease, have mostly normal attributes. This worked opposite to the first question, as we looked for readings in the average range for each attribute.

![NormalGraph](https://user-images.githubusercontent.com/90229634/144931570-2421ca70-7d4f-4753-bb6b-bfa3b816006e.png)

The above graph displays the percentage of each "normal" attribute among patients with a diagnosed heart disease. As you can see, almost 80% of patients with heart disease have a normal fasting blood sugar level. Similarly, the resting ECG level is normal among almost 60% of patients with heart disease. A reason for these results can be due to these attributes being categorical rather than numerical. It isn't as specific as, say, the cholesterol levels where we have a definitive number. We can summarize that RestingECG and FastingBS might not be the most helpful attributes in drawing conclusions or predicting heart disease, though they may still be useful elsewhere in our research.

![AllNormal](https://user-images.githubusercontent.com/90229634/144931588-bd8dc4f6-9612-4bb0-b225-593955a50826.png)

Next, we found all of the patients who displayed almost all their health readings to be completely normal, and still had a diagnosed heart disease. Only three patients tested with these results, and thus can be considered outliers in our study. There may be other factors at play among these patients, whether it be something hereditary or beyond our understanding.

## **Which group of patient(both age and sex) are at the greatest risk?**
![Screenshot (31)](https://user-images.githubusercontent.com/90279551/144963400-f4014644-f20e-4f74-86b1-64e0a8ee5ebd.png)
![Screenshot (32)](https://user-images.githubusercontent.com/90279551/144963415-f21578f5-b169-4f4d-8f53-7adc4a329751.png)

From this first age bracket we can see that the number of young adult males with heart disease is more than double that of young adult females. A possibly correlated factor is the percent of young adult males with unhealthily high levels of cholesterol, which again is more than double the young adult females percentage. The only attribute in which the females have a higher proportion is high resting blood pressure, where it is greater than the male proportion by about a factor of 1/3.

![Screenshot (33)](https://user-images.githubusercontent.com/90279551/144963940-58c14d42-021e-4180-a34b-48a3b3e8cf1a.png)
![Screenshot (34)](https://user-images.githubusercontent.com/90279551/144963942-21fcaf8b-5324-4362-8b77-56d54575c7f2.png)

From the second age bracket, we see a similar pattern to the first in which the male percentages are all (or almost all) greater than their female counterparts. However the sex differences are much smaller within the middle aged bracket. What's interesting is that within this age range, the proportion of males with heart disease is approximately four times larger than the proportion of females with heart disease.

![Screenshot (35)](https://user-images.githubusercontent.com/90279551/144964242-87d49398-17a8-4379-8b29-f13210dd93a9.png)
![Screenshot (36)](https://user-images.githubusercontent.com/90279551/144964245-24b87b2f-99c5-4244-9dde-062e63a512d9.png)

From the final age bracket we can see that all around, the percentage of dangerous attributes has skyrocketed for both males and females. Again we see the males have a massively larger proprotion of people with heart disease, although for this age range, the females have a higher proportion of both high resting blood pressure as well as high cholesterol.

Overall, the senior males (aged 50+) are at the highest risk for heart failure. They have the highest proportion of heart disease, as well as the largest proportion of excercise induced angina. While they are behind the senior women in high cholesterol and high blood pressure, it is not by much which puts them at number 1 for heart failure risk factor.

## **Which attributes appear more frequently in people with heart disease?**
![Screenshot (37)](https://user-images.githubusercontent.com/90279551/144964823-1700b8b4-ab42-4bd8-8321-7cd2b9bebdb9.png)

From the graph above, we can see that patients with heart disease have a higher proportion of having high cholesterol, high resting blood pressure, high fasting blood sugar level, and they are more likely to recieve ST or LVH results on their electrocardiogram.

![Screenshot (38)](https://user-images.githubusercontent.com/90279551/144965089-0b675185-0b65-4f1c-af9d-59552d76de12.png)

This graph shows a much higher proportion of people with heart disease having either asymptomatic chest pain or exercise induced angina. This logically makes sense, as it would explain why so many people don't find out about their heart disease until too late. The high proportion of exercised induced angina also makes sense when you factor in that exercise (especially cardio) puts your heart into situations of extreme stress, which is what is most likely causing the angina.

### **What is the correlation between resting blood pressure and resting ECG results?**

![image](https://user-images.githubusercontent.com/90279551/144968716-ad6420b4-0df3-4285-a31c-c2528d9b0c2d.png)
![image](https://user-images.githubusercontent.com/90279551/144968732-98bb7813-61d5-4cf1-b1b5-56e45a3c433e.png)
![image](https://user-images.githubusercontent.com/90279551/144968748-49b4daa2-d905-4f44-b3e1-69224c8831f1.png)

![image](https://user-images.githubusercontent.com/90279551/144968772-db6411dc-6928-44f7-954d-a4caa052a63a.png)
![image](https://user-images.githubusercontent.com/90279551/144968795-78ffb91c-756c-4747-8ec6-9d59548088ee.png)

![image](https://user-images.githubusercontent.com/90279551/144968813-a707cdfa-5822-40e6-8232-8adcb52d5c75.png)
![image](https://user-images.githubusercontent.com/90279551/144968829-9075c7f7-96b3-4436-a252-8a38dee53979.png)
![image](https://user-images.githubusercontent.com/90279551/144968851-441e4456-f437-4798-a184-2f2cbe5fc541.png)
![image](https://user-images.githubusercontent.com/90279551/144968865-ab169aa3-505f-4885-8623-d7adaeb098c8.png)



### **Which single attribute can be observed as a leading factor towards heart disease?**
![Screenshot (39)](https://user-images.githubusercontent.com/90279551/144966110-64f930f6-a980-49a6-8996-4835d3e5b30b.png)
![Screenshot (40)](https://user-images.githubusercontent.com/90279551/144966133-2e4caed4-86f1-44e4-af45-d1af4f6c36f0.png)

From these two graphs we can see that generally all of the dangerous attributes are slightly higher in people with heart disease. This makes it a problem when trying to identify a single attribute that can mainly predict heart failure/disease, as there is not a large amount of differences between the various attributes proportions.

![Screenshot (41)](https://user-images.githubusercontent.com/90279551/144966301-e262646e-1e96-401d-b221-63705c5621e6.png)
![Screenshot (42)](https://user-images.githubusercontent.com/90279551/144966306-1013bbcc-5e74-4c8f-8043-e24f040c7bdc.png)

Here, we can see that both asymptomatic chest pain and exercise induced angina are found in a much larger proportion in people with heart disease. For obvious reasons, asympotomatic chest pain cannot be used as a leading factor for identifying heart disease, however exercise induced angina has a huge amount of contrast between the proportions of those with heart disease and those without. Due to it having such a large difference, it is a very accurate attribute to select as a leading factor in predicting heart disease. Logically speaking as well, exercised induced angina is most likely one of the earlier symptoms to show up, as it only occurs during moments of high stress to the heart, not all the time like some of the other (most-likely) later occuring attributes.

### **Do those without heart disease still have concerning attributes?**
![ConcernHD](https://user-images.githubusercontent.com/90229634/144931991-5595e8a4-2272-4aeb-b5cb-83086df3c7e3.png)

This first graph is of those without heart disease which we will use to observe trends and draw conclusions.

![ConcernHD2](https://user-images.githubusercontent.com/90229634/144932005-c6553f10-c075-4171-beff-80d265f2814f.png)


This second graph is of those with heart disease which we will use to determine which trends are and are not present in the attributes for both patients with and without heart disease. 

![AllConcern](https://user-images.githubusercontent.com/90229634/144932023-7369af8b-9ab9-441a-adf5-49dcc298bf92.png)

This third graph is of the total population, or the average between the previous two graphs, which we will use as a base case or a default to compare with the other graphs.

With all three graphs we can see that majority of patients with and without heart disease have a high resting blood pressure, a high cholesterol level however they have high fasting blood sugar. 
Unique only to those with heart disease is exercise angina and non-normal resting electrocardiogram.
When compared to patients without heart disease we can see that the non-majority of patients without heart disease have exercise angina and a non-normal resting electrocardiogram.

To conclude patients without heart disease do still have concerning attributes such as a high resting blood pressure and high cholesterol
Patients without heart disease are unlikely to have a non-normal resting electrocardiogram and a high fasting blood sugar. Only a small portion of patients without heart disease have exercise angina. 

## **Is there a noticable difference between those with heart disease and those without when comparing types of chestpain?**

![ChestPainHD](https://user-images.githubusercontent.com/90229634/144932036-c9a105b8-4e6b-487f-85b2-1f1b66bfdb24.png)

When looking at graph 1 we can see a clear majority of the types of chest pain for patients with heart disease. We can see that a patient is about 75% likely to be Asmptomatic, which is far greater than the other chest pain types. We cant make any conclusions just yet from one graph.

![ChestPainHD2](https://user-images.githubusercontent.com/90229634/144932090-38f925a8-ab72-4f4f-8191-34d140821546.png)


Looking at graph 2 we can see that asymptomatic chest pain is not the majority of the chest pain types, rather Atypical Angina is followed by Non-Anginal Pain and then Asymptomatic, Typical Angina is significantly lower than the rest.

Using the information from graph 2, we can confirm that the large percent of Asymptomatic is unique to those with heart disease.
- We could conclude that there is infact a difference between those with and without heart disease when it comes to chest pain types.
- We can also conlcude a large number of people with heart disease go unnoticed, though its possible that the sample size may not be large enough to represent global populations.

## **Conclusion:**
### **Reflection:**
Throughout our data analysis, we learned a lot about cardiovascular health and issues. The biggest lesson we learned was that many heart related issues can go unnoticed, and that it's extremely important to get regular checkups to ensure you are in good health. As studied with asymptomatic patients, you can still be at great risk even if you don't feel like it.

### **Refinement:**

If we were to improve this project, we believe it would be benefitial to include more than one dataset. To fully understand heart related issues, there are a lot more aspects to explore. Looking for either more datasets with overlapping attributes or more sets of data in general, will vastly improve our results. Heart failure can arise from aspects outside of the 12 attributes we explored. Notably, the attrbutes we explored were mostly measured, health related values. We could benefit from external observations to conclude other factors. For example, heart failure may arise from fatigue or exercise related activities. If we were to include a dataset with physical activity and its correspondence with some health issues, we may be able to figure out what physical activities may be dangerous for people at risk.

## Acknowledgements
*This project was submitted as the final course project for CSCI 2000U “Scientific Data Analysis” during Fall 2021. The authors certify that the work in this repository is original and that all appropriate resources are rightfully cited.”*

## README
**Installation:**

In order to fully run our code, you must first download the "Heart Failure Prediction Dataset." The file is uploaded within this repository, or it can be found at: https://www.kaggle.com/fedesoriano/heart-failure-prediction and can be downloaded as a .csv file. The file must be placed in the same location as the FinalProjectGroup28.ipynb notebook.

**Usage:**

To reproduce the results we made, simply run each code cell starting from the top of the notebook moving downward. It is crucial that the user runs the first code cell initially, as this is what loads in the dataset.
