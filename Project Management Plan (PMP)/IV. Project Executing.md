# PROJECT EXECUTING
### Deliverables
#### Software Requirement:
- Python Language
- HyperText Markup Language (HTML)
### Milestone Chart
#### Microsoft Project:
#### Power Point:
### Flowchart
### Description: File, Coding and Implementation
#### 1. Dataset  
This folder contains dataset named News.csv. This project's dataset was obtained via the Kaggle platform at https://www.kaggle.com/techykajal/fakereal-news. This dataset has six attributes, with News Headline being the most crucial for classifying news as FALSE or TRUE.<br>
• News Headline: includes data requiring analysis. <br>
• Link Of News: the URL of the news headline given in the first column.<br>
• Source: This column lists the names of the individuals who posted the news on Facebook,  Instagram, Twitter, or any other social media platform.<br>
• Stated On: The date on which the authors published the news on various social media channels.<br>
• Date: This column indicates the date on which the PolitiFact fact-checking team investigated the information to determine whether it was FALSE or TRUE.<br>
•Label: This column has five class labels: True, Mostly-True, Half-True, Barely-True, False, and Pants on Fire.
#### 2. Data Preprocessing
This folder includes one Python script and one csv file:<br>
1. Text Pre-processing with stopwords.ipynb <br><br>
*Libraries and Packages Required:* <br>
![requirements](https://user-images.githubusercontent.com/121302293/210123593-8c25e0da-a828-4858-83db-58ec1813fe78.png)<br><br>
Before we begin the continuous coding, we must import all necessary libraries. <br>
![1](https://user-images.githubusercontent.com/121302293/210150398-8b4fc9b8-18f7-4d2c-a31d-ae09c748adda.png)<br><br>
The code below is created to read the dataset and print its information.<br>
![2](https://user-images.githubusercontent.com/121302293/210150378-47d86cac-0152-4c35-a634-b7e4be57089f.png)<br><br>
This command displays the non-null values of attributes inside the dataset. <br>
![3](https://user-images.githubusercontent.com/121302293/210150423-106b3f1b-943c-42c6-9f22-078810ade735.png)<br><br>


2. Cleaned_Data.csv
#### 3. Data Visualization
This folder includes  onr Python script **"Visualization_with_Stopwords.ipynb"**. <br>
The primary purpose of this Python script is to explore the dataset's data analysis. This data analysis will provide information regarding the number of columns that contain valuable features, the significance of each feature concerning the problem statement you wish to solve, the distribution of the data per label, and the identification of frequent word counters in both instances labelled "Fake News" and "Real News."
#### 4. ML Pipeline & Deployment
This folder includes two Python script, one pkl file and txt file:
1.Fake_News_Det.py
The code is used to deployment purpose.
2.Modelling With Stopwords.ipynb
This script consists of two sections for development purpose: 
  - Constructing a machine-learning pipeline.
  - Selecting the most suitable Machine Learning models.
3.Model.pkl
The final best model that was selected for the production in the deployment stage. 
4.Requirements.txt
The list of all the required libraries for the project.
### Result <br>
1. Running the **"Fake_News_Det.py"**. A interactive dashboard will appear like follows:
![Fake_News_Detector](https://user-images.githubusercontent.com/121302293/210138580-2aa39285-455c-4b69-8f8a-a688eb45b27f.png) <br><br>
2. Input one part of the news for which you would like to see results:
![Fake_News_Detector_with_News](https://user-images.githubusercontent.com/121302293/210138594-dc5e1669-65d4-458a-8f4f-a305d28eb7e8.png)<br><br>
3. "Fake News" or "Real News" will display. 
![Fake_News_Detector_Result](https://user-images.githubusercontent.com/121302293/210138601-cb5018cd-4c9d-45a6-8e31-056fc4094fdb.png)

&nbsp;<br>
&nbsp;<br>
&nbsp;<br>
:arrow_right:: [Project Monitoring and Controlling](https://github.com/FilleHeureuse/Fake-News-Detection-System/blob/main/Project%20Management%20Plan%20(PMP)/V.%20Project%20Monitoring%20and%20Controlling.md)
