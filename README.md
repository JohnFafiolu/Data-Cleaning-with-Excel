# Data-Cleaning-with-Excel
## Data Overview
The dirty dataset which I got from Kaggle contains over 2,000 job listings for data analyst positions, sourced from a publicly available repository. Key Columns include:
- Salary Estimate: Ranges for potential earnings.
- Location: City and state where the job is based.
- Company Rating: Employer ratings from current and former employees.
- Job Description: Detailed requirements and responsibilities for each role.
- [Get Dataset Here](https://www.kaggle.com/datasets/andrewmvd/data-analyst-jobs)


![Screenshot 2024-12-23 111639](https://github.com/user-attachments/assets/0b284e05-e1fe-4d00-a2c3-9c2199bab8cc)

### Tool Used
- MS Excel
- Power Query
## Methodologies
- The first step I took was to organize the dataset by spacing out all the columns and importing it into Power Query for cleaning.  

 ![Screenshot 2024-12-22 113427](https://github.com/user-attachments/assets/0b32a195-801c-4503-b59c-8b747c73b608)
 
- In Power Query, I cleaned and trimmed all text entries to eliminate unnecessary white spaces and newline characters. I set the first column as the header and cleaned up company names that had unusual numbers appended to them.  

- For cells in the *Type of Ownership* column containing both numbers and "unknown," I replaced the values with "Other Organizations." Additionally, I standardized names for private organizations by renaming all variations (e.g., "Private Practice/Firm") to simply "Private." Similarly, I consolidated entries like "College/University" into "School" for consistency.  

- I split the *Location* column into two separate columns: one for city and one for state.
- In the *Job Description* column, I removed all non-alplicable characters and retained only letters and spaces using Power Query formulas.

```m
Text.Select([Job Description],{"A".."z",",","-","."," ","-"})
```
- I did the same for the company Name column
```m
Text.Select([Company Name],{"A".."z"," "})
```

- For columns like *Company Size*, *Sector*, and *Industry*, I replaced numeric entries with "Unknown" to ensure consistency in categorical data.  

The cleaned dataset isnow well-structured and ready for any further analysis.  
![Screenshot 2024-12-23 120622](https://github.com/user-attachments/assets/41c981e8-68bd-4211-a4a9-cbf32e92f541)
![Screenshot 2024-12-23 120749](https://github.com/user-attachments/assets/eafd163b-df5c-40ab-8dd1-a7b85517e496)

 
