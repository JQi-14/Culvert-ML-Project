# Culvert-ML-Project
This is the folder for sharing of data and python codes.<br/>
***
The difference between the two <code>csv</code> files is that one contains un-transformed raw data, the other has all values scaled by the maxmin method.

To load the data here on Jupyter, use the **raw** form of the data as shown in the figure below.<br/>
<img src="https://github.com/JQi-14/Culvert-ML-Project/blob/main/Misc./note.png?raw=true" />
Example Python codes:<br/>
<code>data=pandas.read_csv('https://raw.githubusercontent.com/JQi-14/Culvert-ML-Project/main/686_full_data_raw_03_21_22.csv')</code><br/>


## Access to Dr. Andrew Ng's ML courses
https://www.coursera.org/specializations/machine-learning-introduction <br/>
You do not have to purchase a subscription to enroll in any of the courses. There are three courses listed on this webpage. 
Go to each individual course’s sub-page (i.e. 'Supervised Machine Learning: Regression and Classification'; 'Advanced Learning Algorithms'; and 'Unsupervised Learning, Recommenders, Reinforcement Learning') and click ‘enroll for free’. Choose ‘audit the course’ at the bottom of the pop-up dialog. <br/>

<img src="https://github.com/JQi-14/Culvert-ML-Project/blob/main/Misc./corsara.png?raw=true" />

## Understanding the raw data 686_full_data_raw_06_28_22.csv
1. Total sample size is 686 currently<br/>
2. Column A gives the identifiers of all records and does not contribute to the prediction result. <br/>
3. Columns D and G are nominal type data; column H is ordinal type data.<br/>
4. Columns M, P, Q, and R are calculated based on variables listed on the left of it, meaning you do not have to use this column.<br/>
5. Columns S to AC are the data provided by the CMSWS and can (all or partially) be considered as output variables. The main relationship among them is that <br/>
         a. Risk = LOF * COF    - (Overall)<br/>
         b. Flood Risk = Flood LOF * Flood COF  - (flood)<br/>
         c. CON Risk = CON LOF * CON COF  - (condition)<br/>
         d. (overall) LOF and COF are determined based on flood and condition LOF and COF, the calculation method by CMSWS is detailed in 2_Raw_Data\Output Data – CMSWS<br/>

Feel free to try out any of them as possible output variables. Note that Columns N and O are duplicated in Columns U and Z<br/>

6. Columns I and J are somewhat related: Column I is the evaluation of how much clogging is observed, and Column J evaluates if it has caused floods due to the clogging (binary results). <br/>
