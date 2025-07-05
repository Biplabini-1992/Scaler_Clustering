# Scaler Learner Clustering & Company Profiling
## Objective
Scaler, a tech-versity by InterviewBit, offers advanced computer science and data science courses aimed at upskilling software professionals. As part of the analytics team, your task is to profile the best companies and job positions using learner data.

The goal is to perform manual clustering and unsupervised learning techniques (K-Means, Hierarchical Clustering) to identify:

- Patterns in compensation
- High-performing roles or departments
- Company-wise pay structures
- Learners outperforming their peers

## Dataset Information
### Features:
  - Unnamed: 0: Index
  
  - Email_hash: Anonymized learner identifier
  
  - Company_hash: Anonymized employer/company identifier
  
  - orgyear: Employment start year
  
  - CTC: Current Cost To Company
  
  - Job_position: Learner's job title
  
  - CTC_updated_year: Year of latest CTC update

## Project Workflow
### 1. Exploratory Data Analysis (EDA):
  - Structure & summary statistics
  
  - Unique emails and frequency analysis
  
  - Missing value analysis
  
  - Regex cleaning (e.g., removing special characters)
  
  - Duplicate record handling

### 2. Feature Engineering:
  - Creation of Years_of_Experience = CTC_updated_year - orgyear
  
  - Manual Clustering based on:
  
    - Company
    
    - Job Position
    
    - Years of Experience

### 3. Summary Statistics & Flags:
  - 5-point summary (mean, median, min, max, count) of CTC grouped by:
    
    - Company
    
    - Job Position
    
    - Years of Experience
  
  - Creating classification flags:
  
    - designation: Based on experience & CTC (1: Above Avg, 2: Avg, 3: Below Avg)
  
  - Class: Job Position + Company based flag
  
  - Tier: Company-level flag

### 4. 🏅 Manual Clustering Insights:
  - Top 10 high-tier earners (Tier 1)
  
  - Top/Bottom 10 learners in Data Science (Class 1 / Class 3)
  
  - Tier-based comparison within company-department-Experience (e.g., Tier X)
  
  - Top 10 companies by average CTC
  
  - Top 2 high-paying job positions per company

### 5. 🤖 Unsupervised Clustering:
  - Label Encoding & One-Hot Encoding
  
  - Standardization of data
  
  - Clustering Tendency Check
  
  - K-Means Clustering
  
  - Elbow Method for optimal K
  
  - Hierarchical Clustering
  
  - Applied on a sample if needed due to performance

## Key Insights & Business Recommendations
  
  - Identify underpaid and overpaid roles
  
  - Highlight high-performing departments or job titles
  
  - Recognize top-tier companies for various experience levels
  
  - Support learners in benchmarking salaries
  
  - Help companies align compensation with market trends

## Technologies Used
- Language: Python 3.x

- Libraries:
  
  - pandas, numpy – Data wrangling
  
  - matplotlib, seaborn – Visualization
  
  - sklearn – Clustering, Standardization
  
  - scipy – Hierarchical clustering
  
  - re – Regex for text cleaning
