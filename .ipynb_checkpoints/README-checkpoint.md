# AI skills per job industry postings on LinkedIn between 2023-2024

This data journalism project looks at how employer demand for AI skills spans a wide range of industries. 

## Byline and Credits 

**By:** Sabrina Ortiz 
**Affiliation:** Craig Newmark School of Journalism 

**Date:** 2025 

## Project Summary 

The LinkedIn data used for the report came from a dataset posted on Kaggle which contained a record of 124,000+ job postings listed in 2023 and 2024, which the user compiled by using LinkedIn’s backend search API to retrieve the most recent job postings and their attributes. In the dataset collection, the uploader does disclose that the dataset is “nearly” comprehensive, with there being the possibility of sporadic postings being omitted during peak hours. However, the data still serves as a large representative sample of LinkedIn jobs.

## Methodology 

To clean the dataset, first I dropped any rows in the jobs datasets that had “N/A” in the description, as my analysis was dependent on looking at the mentions of the keywords in the description of the job postings. Then, for consistency, I dropped any job postings in which the job was posted under multiple industries as this analysis is looking specifically at the demand for AI skills in specific industries, and if the same job is accounted for twice it would have skewed the results. 

The jobs postings dataset did not have the industries listed, so I had to merge the separate industries dataset to the original job postings one, matching it by job listings. Once there was one larger dataset, I created a column to identify whether a job description contains keywords related to AI. The keywords I used as the identifier included AI, machine learning, artificial intelligence, generative AI, deep learning, and large language models. This filtering was set to be case sensitive as the letters “ai” are in many words. This does mean that it is possible that some listings which include the key terms at the beginning of the sentence may have been left out. 

This filtering means that there is the possibility that some job descriptions mentioned “AI” for other reasons, such as using AI to filter applications, describing their companies, or forbidding the use of AI in the application. To account for this, out of the job postings which were identified as having AI, I took a random sample of 5% of them and manually read each one to see if the mention of AI related to skills or other. In a super majority of the random sample (66%), it was an accurate tag. Another 29.8% mentions of AI were used to describe the company, which is noteworthy because it signifies how companies from different industries are virtual signaling that they use AI in alignment with the trends, and even if the company isn’t looking for AI skills directly, these applicants may be interacting with AI anyways because of the nature of the company. 
Lastly, I created a new data frame that shows the percentage of job descriptions in each industry group that mention one of the AI keywords.

## Additional resources

Github link: https://github.com/sabrinaa-ortiz/Advanced-DataReportingFinal/tree/main
Dataset source: https://www.kaggle.com/datasets/arshkon/linkedin-job-postings?resource=download