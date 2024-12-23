# Data-Cleaning-with-Excel
## Data Overview
The dirty dataset which I got from Kaggle contains over 2,000 job listings for data analyst positions, sourced from a publicly available repository. Key Columns include:
- Salary Estimate: Ranges for potential earnings.
- Location: City and state where the job is based.
- Company Rating: Employer ratings from current and former employees.
- Job Description: Detailed requirements and responsibilities for each role.
- [Get Dataset Here](https://www.kaggle.com/datasets/andrewmvd/data-analyst-jobs)

[DataAnalyst.csv](https://github.com/user-attachments/files/18228269/DataAnalyst.csv)


### Tool Used
- MS Excel
- Power Query
## Methodologies
- The first step I took was to organize the dataset by spacing out all the columns and importing it into Power Query for cleaning.  

- In Power Query, I cleaned and trimmed all text entries to eliminate unnecessary white spaces and newline characters. I set the first column as the header and cleaned up company names that had unusual numbers appended to them.  

- For cells in the *Type of Ownership* column containing both numbers and "unknown," I replaced the values with "Other Organizations." Additionally, I standardized names for private organizations by renaming all variations (e.g., "Private Practice/Firm") to simply "Private." Similarly, I consolidated entries like "College/University" into "School" for consistency.  

- I split the *Location* column into two separate columns: one for city and one for state. In the *Description* column, I removed all non-alphabetic characters and retained only letters and spaces using Power Query formulas.  

- For columns like *Company Size*, *Sector*, and *Industry*, I replaced numeric entries with "Unknown" to ensure consistency in categorical data.  

The cleaned dataset is now well-structured and ready for any further analysis.  
