# Machine Learning for Culvert Condition Prediction Project
$\color{black}{\text{PI: Dr. Nicole Barclay and Dr. Michael Smith}}$<br/>

$\color{green}{\text{Hi team, welcome aboard!}}$<br/>
<br/>
<br/>
$\color{green}{\text{In this repository, you will find data and maybe python codes for our ML project.}}$<br/>
$\color{green}{\text{You can also upload your own if you'd like.}}$<br/>
If you have any questions, contact Jenny (jqi1@uncc.edu).


***

## How to use it
To load the data here onto your Jupyter notebook, use the **raw** form of the data as shown in the figure below.<br/>
<img src="https://github.com/JQi-14/Culvert-ML-Project/blob/main/Misc./note.png?raw=true" />
Example Python codes:<br/>
<code>data=pandas.read_csv('https://raw.githubusercontent.com/JQi-14/Culvert-ML-Project/main/686_full_data_raw_03_21_22.csv')</code><br/>

## Understanding the data in '686_full_data_raw_06_28_22.csv' (see below for the newer versions of the dataset)
1. Total sample size is 686<br/>
2. Column A gives the identifiers of all records and does not contribute to the prediction result. <br/>
3. Columns D and G are nominal type data; column H is ordinal type data.<br/>
4. Columns M, P, Q, and R are calculated based on variables listed on the left of it, meaning you do not have to use this column.<br/>
5. Columns S to AC are the data provided by the CMSWS and can (all or partially) be considered as output variables. The main relationship among them is that <br/>
         a. Risk = LOF * COF    - (Overall)<br/>
         b. Flood Risk = Flood LOF * Flood COF  - (flood)<br/>
         c. CON Risk = CON LOF * CON COF  - (condition)<br/>
         d. (overall) LOF and COF are determined based on flood and condition LOF and COF, the calculation method by CMSWS is detailed in 2_Raw_Data\Output Data – CMSWS<br/>
See the calculation flow chart below for details.<br/>
Feel free to try out any of them as possible output variables. Note that Columns N and O are duplicated in Columns U and Z<br/>
6. Columns I and J are somewhat related: Column I is the evaluation of how much clogging is observed, and Column J evaluates if it has caused floods due to the clogging (binary results). <br/>
<img src="https://github.com/JQi-14/Culvert-ML-Project/blob/main/Misc./Calculations%20Flow%20Chart.jpg?raw=true" />

## Understanding the data in 'Culvert Max Records Full Dataset 082522.csv'
This dataset is 100% raw, meaning the only process it went through was joining the data from different sources. Only calculation was for 'age at inspection date' using the difference between 'construction date' and 'inspection date'. No corrections were made, so there are some apparently inaccurate values. The detailed data joining processes are provided in </b>"2_Raw_Data\Notes and Summaries\Data joining - keep max records (1265).docx"</br>

## Understanding the data in 'Max Records Full Dataset minorly corrected.csv'
This dataset has a minor degree of QA filters for missing data or incorrect data comparing to the one mentioned directly above. Check the 'metadata' tab in the excel file with the same name for detailed explanations/justifications. Because it is minimally processed, the correlations between input variables and the target variable is very low (i.e., the performances of your models may be undesirable even after parameter tunning). It *might* mean that data engineering is necessary. <br/>

## Access to Dr. Andrew Ng's ML courses
https://www.coursera.org/specializations/machine-learning-introduction <br/>
You do not have to purchase a subscription to enroll in any of the courses. There are three courses listed on this webpage. 
Go to each individual course’s sub-page (i.e. 'Supervised Machine Learning: Regression and Classification'; 'Advanced Learning Algorithms'; and 'Unsupervised Learning, Recommenders, Reinforcement Learning') and click ‘enroll for free’. Choose ‘audit the course’ at the bottom of the pop-up dialog. See the screenshot below<br/>
Someone made some superb notes for his courses (mainly on NN) avalable in their repository. Check it out --> https://github.com/ashishpatel26/Andrew-NG-Notes
<img src="https://github.com/JQi-14/Culvert-ML-Project/blob/main/Misc./corsara.png?raw=true" />
