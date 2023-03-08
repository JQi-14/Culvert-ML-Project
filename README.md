# Machine Learning for Culvert Condition Prediction Project
<font color=black size='4'>PI: Dr. Nicole Barclay and Dr. Michael Smith</font><br/>
<br/>

<br/>
<font color=green size='4'>In this repository, you will find data and python codes for our ML project.</font><br/>
If you have any questions, contact Jenny (jqi1@uncc.edu).


***

## How to use it
To load the data here onto your Jupyter notebook, use the **raw** dataset URL by clicking the button. 
If you want to download any files, right click and choose 'save as'<br/>
Example Python codes:<br/>
<code>data=pandas.read_csv('https://raw.githubusercontent.com/JQi-14/Culvert-ML-Project/main/dataset.csv')</code><br/>


## Understanding the dataset
This dataset is raw, the process it went through was joining the data from different sources in ArcGIS and the only calculation was for 'age at inspection date' using the difference between 'construction date' and 'inspection date'. The detailed data joining processes are provided in **"2_Raw_Data\Notes and Summaries\Data joining - keep max records (1265).docx"**.This dataset has a minor degree of QA filters for missing data or incorrect data. Check the 'metadata' tab in the excel file with the same name for detailed explanations/justifications. <br/>

