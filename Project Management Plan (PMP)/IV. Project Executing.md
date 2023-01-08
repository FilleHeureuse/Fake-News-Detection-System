# PROJECT EXECUTING
### Software Requirement
- Python Language
- HyperText Markup Language (HTML)
### Task and Estimated Cost
| **Task** | **Estimated Cost** |
|:-------|:------:|
|Project Manager|RM5000|
|Project Team Members|	|
|  1.	Procurement Manager|RM3500|
|  2.	Risk Manager|RM3500|
|  3.	Administrative Manager|RM3500|
|  4.	Financial Analyst	|RM2500|
|  5.	Project Scheduler	|RM2500|
|  6.	Quality Manager|RM3500|
|Installation Software|RM5500|
|Licensed Software|RM4000|
|Testing	|RM13000|
|System maintenance|RM10000|
|**Total Project**|	RM56500|
### Milestone Chart
![image](https://user-images.githubusercontent.com/121302293/210359830-75d378b4-ae73-4e81-93ea-fa458a188f3b.png)
![image](https://user-images.githubusercontent.com/121302293/210359846-1f4c3d42-c817-4f8e-9306-499c53928a8a.png)
### Flowchart
![image](https://user-images.githubusercontent.com/121302293/210193305-fb737e10-c070-49f5-9174-3b758c3a8be4.png)
### Description: File, Coding and Implementation
#### 1. Dataset  
This folder contains dataset named News.csv. This project's dataset was obtained via the Kaggle platform at https://www.kaggle.com/techykajal/fakereal-news. This dataset has six attributes, with News Headline being the most crucial for classifying news as FALSE or TRUE.<br><br>
| **Attributes** | **Responsibilities** |
|:-------:|------|
| News Headline | Include data requiring analysis. |
| Link Of News | The URL of the news headline given in the first column. |
| Source | This column lists the names of the individuals who posted the news on Facebook,  Instagram, Twitter, or any other social media platform. |
| Stated On | The date on which the authors published the news on various social media channels. |
| Date | This column indicates the date on which the PolitiFact fact-checking team investigated the information to determine whether it was FALSE or TRUE. |
| Label | This column has five class labels: True, Mostly-True, Half-True, Barely-True, False, and Pants on Fire. |
#### 2. Data Preprocessing
Preprocessing data is an important step for data analysis. 
<ul><li>It improves accuracy and reliability. It can improve the accuracy and quality of a dataset by removing inconsistent or missing data values due to human or computer error.</li><li>It makes data consistent. In the process of collecting data, duplicates are possible. Discarding them during preprocessing is an effective way to ensure that the <data values for analysis are consistent, allowing the results to be as accurate as possible.</li><li>The algorithm becomes easier to read as a result. Preprocessing data enhances its quality and makes it easier for machine learning algorithms to read, use, and interpret it.</li></ul>
This folder includes one Python script and one csv file:<br>

1. **Text Pre-processing with stopwords.ipynb** <br><br>
*Libraries and Packages Required:* <br>

Before analysing the data, there several preprocessing steps need to be done.
* Remove Emojis 
![6](https://user-images.githubusercontent.com/121302293/210193860-2b20f148-db92-4880-8f24-f6f7ef59ca2a.png)
* Remove NewLines & Tabs
![7](https://user-images.githubusercontent.com/121302293/210193956-c59727f9-e47b-40d7-8c0a-efc6dc29a916.png)
* Remove Strip HTML Tags
![8](https://user-images.githubusercontent.com/121302293/210193968-6fafdeda-c3fa-4f95-ba9e-59c30694f37c.png)
* Remove Links
![9](https://user-images.githubusercontent.com/121302293/210193976-13c05d11-61fb-481c-948e-3f391099bd58.png)
* Remove WhiteSpaces
![10](https://user-images.githubusercontent.com/121302293/210193991-05ea8984-d166-40bf-92de-5b39bdf98b25.png)
* Remove Accented Characters, Case Conversion (to lowercase)
![11](https://user-images.githubusercontent.com/121302293/210194023-b49e21a9-f7ea-439c-9574-97ca157e7b8c.png)
* Reduce Repetaed Characters and Punctuations
![12](https://user-images.githubusercontent.com/121302293/210194045-2f5237ff-3e6c-4369-9bd1-bd510d37c57f.png)
   Explanation for using some symbols in above regex expression:<br><br>
   | **Symbols** | **Description** |
   |:-------:|-------------|
   | \1 | Is equivalent to re.search(...). group(1). It Refers to first capturing group. \1 matches the exact same text that was matched by the first capturing group.|
   | {1,} | It means we are matching for repeatation that occurs more than one times.|
   | DOTALL | It matches newline character as well unlike dot operator which matches everything in the given text except newline character. |
   | sub() | This function is used to replace occurrences of a particular sub-string with another sub-string. This function takes as input the following: The sub-          string to replace. The sub-string to replace with. |
   | r'\1\1' | It limits all the repeatation to two characters. |
   | r'\1' | Limits all the repeatation to only one character. |
   | {2,} | It means to match for repeatation that occurs more than two times. |
* Expand Contraction Words<br><br>
![13](https://user-images.githubusercontent.com/121302293/210194921-d9a2c48e-cfbd-48b5-a125-6fdf4575a9f9.png)
![13a](https://user-images.githubusercontent.com/121302293/210194925-76002714-c895-4d5b-a71d-53272a091285.png)
![13b](https://user-images.githubusercontent.com/121302293/210194981-f3b0fb02-7d71-49a8-95c5-db21c7d81f35.png)
* Remove Special Characters
![14](https://user-images.githubusercontent.com/121302293/210194089-c04f673d-7833-43e6-b5ca-44686d7d2342.png)
   | **Punctuation** | **Description** |
   |:-------:|--------|
   | ,.?! | These are some frequent punctuations that occurs a lot and needed to preserved as to    understand the context of text. |
   | : | This one is also frequent as per the Dataset. It is important to keep bcz it is giving    sense whenever there is a occurrence of time like: 9:05 p.m. |
   | % | This one is also frequently used in many articles and telling more precisely about the    data, facts & figures. |
   | $ | This one is used in many articles where prices are considered. So, omitting this symbol    will not give much sense about those prices that left as just some     numbers only. |
* Remove Stopwords
![15](https://user-images.githubusercontent.com/121302293/210194099-6d0e2238-0dbe-4982-a2a8-366fdceeaa62.png)
* Correct Mis-Spelled Words in Text
![16](https://user-images.githubusercontent.com/121302293/210194107-68d523e2-2b0a-451e-ab2b-eb56ef5615e6.png)
* Lemmatization <br><br>
![17](https://user-images.githubusercontent.com/121302293/210194110-e6580fa9-906d-4e7f-a688-2998a90553b8.png)
After we defined these *Data Normalization* techniques, we combine them into a single function.<br><br>
![18](https://user-images.githubusercontent.com/121302293/210194152-0b3cafc6-3895-4224-bc98-716938830129.png)
2. **Cleaned_Data.csv**<br>
This csv file contains 7754 data and is saved after the data is done preprocessing. This data will be used for data analysis.<br><br>
![image](https://user-images.githubusercontent.com/121302293/210196012-a7e08b8a-32b2-4587-a6b6-0f70fcad73b2.png)
#### 3. Data Visualization
This folder includes  onr Python script **"Visualization_with_Stopwords.ipynb"**. <br>
The primary purpose of this Python script is to explore the dataset's data analysis. This data analysis will provide information regarding the number of columns that contain valuable features, the significance of each feature concerning the problem statement you wish to solve, the distribution of the data per label, and the identification of frequent word counters in both instances labelled "Fake News" and "Real News."<br><br>
**Word Cloud: Fake News**<br>
![image](https://user-images.githubusercontent.com/121302293/210195634-49dd0b6c-b615-49e5-a849-ccc2b62f1be2.png)<br><br>
**Word Cloud: Real News**<br>
![image](https://user-images.githubusercontent.com/121302293/210195650-620c4bdc-fe14-4845-8fef-1746feca0548.png)
#### 4. ML Pipeline & Deployment
This folder includes two Python script, one pkl file and txt file:
1. Fake_News_Det.py<br> 
The code is used to deployment purpose.
2. Modelling With Stopwords.ipynb<br>
This script consists of two sections for development purpose:<br> 
    * Constructing a machine-learning pipeline.<br>
    * Selecting the most suitable Machine Learning models.
3. Model.pkl<br>
The final best model that was selected for the production in the deployment stage. 
4. Requirements.txt<br>
The list of all the required libraries for the project. <br><br>
![requirements](https://user-images.githubusercontent.com/121302293/210123593-8c25e0da-a828-4858-83db-58ec1813fe78.png)
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
