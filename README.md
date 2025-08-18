**Team Number**: 24  
**Course**: CSC4792 - Data Mining  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1b4ILDC_YuD84cm3L4W0sbBEYkx7tk3U2?usp=sharing)
## Team Members
- Musonda Chibuye 2020022320  musonda.chibuye@cs.unza.zm
- Nasaka Fubisha  2021500225  nasaka.fubisha@cs.unza.zm
- Nathan Mbumwae  2021458474  nathan@cs.unza.zm
- Paul Akakandelwa 2020046679  paul.akakandelwa@cs.unza.zm
- Ternwani Mnango  2021432050  temwani.mhango150@cs.unza.zm

## Project Topic
### **2.2.4**: Classify Journal Articles into Zambia's Vision 2030 Sector Categories

# 1. Business Understanding

 ## Problem Statement
 The University of Zambia publishes numerous scholarly articles across various disciplines, but there is no automated system to categorize these publications according to Zambia’s Vision  2030 sector classifications (e.g., Education, Health, Agriculture). This lack of classification makes it difficult for policymakers, researchers, and students to identify research   relevant to national development priorities quickly. Manually sorting articles is time-consuming and prone to human error, limiting the accessibility and impact of academic research.

## **Business Objectives**

1. **Develop an automated classification system**  
   Accurately categorize scholarly articles from the University of Zambia into the official *Zambia’s Vision 2030* sector classifications  
   *(e.g., Education, Health, Agriculture)*.

2. **Improve accessibility of academic research**  
   Enable policymakers, researchers, and students to locate publications relevant to national development priorities quickly.

3. **Reduce manual workload & eliminate classification errors**  
   Provide a consistent, data-driven categorization process to replace human classification.

4. **Enhance the impact of academic research**  
   Align publications with *Zambia’s Vision 2030* goals, making it easier for decision-makers to leverage research for evidence-based policy and planning.
######**Practical Success**
- A policymaker searches for **"Education sector"** in the system and instantly retrieves all University of Zambia publications related to that sector — without having to manually read and sort each article.

- Any user can search for and retrieve articles by the *Vision 2030* sector in seconds.  
- The classification is consistent, accurate, and requires minimal manual intervention.

## **Data Mining Goals**

1. **Build a text classification model**  
   Automatically categorize scholarly articles from the University of Zambia into *Zambia’s Vision 2030* sector categories  
   *(e.g., Education, Health, Agriculture)* based on article titles, abstracts, and keywords.

2. **Preprocess and clean the text data**  
   Remove stop words, apply stemming or lemmatization, and handle special characters to prepare it for machine learning algorithms.

3. **Extract relevant features from the article text**  
   Use Natural Language Processing (NLP) techniques such as **TF-IDF** (Term Frequency–Inverse Document Frequency) or word embeddings.

4. **Train and evaluate classification algorithms**  
   Experiment with models such as **Naïve Bayes**, **Support Vector Machines (SVM)**, or **Logistic Regression** to determine which provides the highest accuracy for this dataset.

5. **Deploy the trained model**  
   Integrate it into a searchable interface that allows users to retrieve articles by *Vision 2030* sector in a short period.

## **Initial Project Success Criteria**

1. **Accuracy Threshold**
     The classification model should achieve **at least 80% accuracy** on the test dataset when categorizing articles into *Zambia’s Vision 2030* sector categories.

2. **Balanced Performance**
     The model must maintain a **minimum precision and recall of 75%** across all sectors to ensure no single category is disproportionately misclassified.

3. **Coverage of All Sectors**
     The system should be able to classify articles into **all major Vision 2030 sectors** (e.g., Education, Health, Agriculture, etc.) without excluding any represented category.

4. **Speed of Classification**
    The model should return results in **a short period** for a single article query to support real-time search functionality.

5. **Reduction of Manual Effort**
     Compared to manual sorting, the automated system should **reduce classification time by at least 70%**, making research retrieval faster and more consistent.

6. **Usable Output**
    The final system should produce a **searchable, categorized dataset or dashboard** for policymakers, researchers, and students, enabling instant filtering by Vision 2030 sector.



# 2. Data Undestanding


We successfully loaded the dataset vision_2030_dataset - unza_journal_articles.csv into a pandas DataFrame.  
- The first 5 rows (df.head()) confirm that column names and sample data appear as expected.  
- The dataset shape (df.shape) shows <number_of_rows> rows and <number_of_columns> columns, which matches our expectations.  

Thus, the dataset is correctly loaded and ready for further exploration.

## 2.4: Summary of Findings

- **Dataset Size**: The dataset contains **124 rows** and **12 columns**.

- **Missing Values / Inconsistencies**:
  - Missing values are present in some columns (e.g., **sector** and **keywords**).
  - Possible **duplicate titles or DOIs** exist.
  - A few year entries may need to be checked for validity.

- **Numerical Columns**:
  - **Year**: Publications range mainly from **2014–2024**, showing growth in scholarly output in recent years.

- **Categorical Columns**:
  - **Sector**: Categories are **imbalanced** — most articles fall under *Education and Skills Development* and *Health*, while other Vision 2030 sectors are underrepresented.
  - **Journal**: A small set of journals dominate; many appear only once.
  - **Authors**: A few prolific authors publish repeatedly, but most appear just once.

- **Potential Data Cleaning Needed**:
  - Fill or drop missing values in **sector, and keywords**.
  - Identify and remove **duplicates** in titles/DOIs.
  - Consider grouping underrepresented **sectors** to balance categories.
  - Normalize or transform **skewed numerical features** like citations.


**Conclusion**:  
The dataset is structured and ready for analysis, but **preprocessing** is necessary to address missing values, duplicates, imbalanced categories, and outliers. Once cleaned, the dataset will support reliable classification and trend analysis.



