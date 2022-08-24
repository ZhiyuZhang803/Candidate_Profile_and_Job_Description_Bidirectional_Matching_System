# Candidate_Profile_and_Job_Description_Bidirectional_Matching_System
- MUST READ: In order to protect our Candidate, this repo doesn't contain any dataset that includes real candidte information. If you need some test cases in any folder/file, please contact the Author (zhiyuzha@usc.edu) for more information!
- This repo contains all files needed for constructing NLP based bidirectional matching system between candidate profile and job description and improve the efficiency as well as the accuracy in matching process.
- This system was first constructed during summer 2022 internship but is improved and will improve continuously.
- If you have any question or just show strong interest towards our project, please do not hesitate to contact the Author via zhiyuzha@usc.edu.
- VERSION0:AUG 8, 2022; 
- VERSION1:AUG 23, 2022; (CREATE THE BASIC FRAMEWORK FOR THE LAST STEP)

## Main Purpose and Brief Introduction:
Matching system is one of the most popular artificial intelligence systems for companies in different industries across the world. As a world-leading recruiting company, we also wants to introduce this kind of system to fill the gap and improve the experience of clients. We aim to construct a bidirectional matching system between recruiter and potential candidates with machine learning techniques (especially advanced NLP techniques), improving the efficiency of recruitment activity and grabbing market share of our start-up.

## Basic Workflow and Algorithms:
- Core Algorithms:
In order to compare the similarity of two text-based content (candidate profile and job description), we need to clean the original dataset (seperate words and remove useless words), vectorize core features (transfor from text to numerical data) and project the vector to pre-defined recruiting matrix (recruiting maxtrix that contains all features we need to evaluate). Finally, calculate cosine similarity between features and select candidate with high number.
- Basic Workflow:
1. Read Candidate Profile and Job Description & transform them to uniform json format
2. Use NLP NER to identify and label the key words occured in the first step
3. Project the key words into predefined recruiting matrix and transform each profile/JD into a vector
4. Calculate the cosine similarities between profile and JD and recommend based on rankings

## Introduction of Files and Datasets in this Repo:
- This repo contains 1 Powerpoint File and 1 Folder (Contains All Code and Data Files). All files and folders will be introduced in this section.

### Powerpoint File
1. File(s): Matching System Detailed Explanation. pptx
2. Content: The detailed introduction and workflow of whole project.

### Matching System Folder

#### Construct Major and Title Datasets Folder
##### Construct Job Title Dataset:
- We use O*NET&zety online resources to construct a cleaned dataset that contains job titles in the market as many as possible.
1. File(s): scrap job title.ipynb -> uncleaned_job_title.xlsx -> clean_jobtitle.ipynb -> title_final.xlsx
2. Content: Get job titles from https://zety.com/blog/job-titles and do data cleaning. Results can be found in the corresponding excel files.
1. File(s): title_final.xlsx & XXX_job_title.xlsx (6 files) -> add_additional_job_titles.ipynb -> title_final.xlsx (cover the previous file with same name)
2. Content: Combine job titles scraped from https://www.onetonline.org with titles from the first step. Result can be found in the corresponding excel files.  
##### Construct Major Dataset
- We use act.org online resource, combined with self-owned dataset, to construct a cleaned dataset that contains majors in the college as many as possible.
1. File(s): webscrap_major.ipynb -> student_major.csv & student_major2.csv -> create student major.ipynb -> major.xlsx
2. Content: Get college major from O * NET and do data cleaning. Result can be found in the corresponding excel files.
1. File(s): major.xlsx & more_majors.xlsx -> add_more_majors.ipynb -> temp_merged_major.xlsx
2. Content: Combined self-owned major dataset with dataset from the first step, continually expand the dataset. Result can be found in the corresponding excel files.

#### Construct Skillset Folder
##### Construct Hardskill Set
- We use O * NET online resoures, combined with some acvanced data processing techniques, to construct a cleaned json-format dataset that can be passed in NLP SpaCy Named Entity Recognition. 143 groups of and over 3000 single items of hardskills can be recognized.
1. Folder(s): active_listening/math/reading_comprehension/science/speaking/writing_position
2. Content: Gather hardskill related information for different types of position from O * NET website. Results can be found in XXX_skillset.xlsx file in each folder.
1. Folder(s): Final_merge&analysis_hardskills
2. Stream of the files: merge_skillset.ipynb -> final_skill_table.xlsx & large software company.csv -> clean_skillset.ipynb -> cleaned_skillset.xlsx -> create_hardskill_dataset.ipynb -> hardskills.json
3. Content: Clean and expand hard skill dataset. Try to cover all possible situations that may occur in profile (e.g. Microsoft Powerpoint, Powerpoint, PPT may point to the same skillset). Readable result can be found in the cleaned_skillset.xlsx and SpaCy usable result can be found in the hardskills.json.
##### Construct Softskill Set
- We use O * NET online resoures, combined with some acvanced data processing techniques, to construct a cleaned json-format dataset that can be used for detecting softskills in original data. 40 groups of and over 2000 single items of hardskills can be recognized.
1. Folder(s): 

#### Profile Cleaning Before Input Folder
- This part may contain some sensitive information, please contact author for test case if you need.
##### Clean Candidate Profile
##### Clean JD Profile

#### Structure and Implementation of Matching System Folder


