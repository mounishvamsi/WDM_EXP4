### EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE: 22-05-2026
### AIM: To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program:
```python
# Visitor segmentation based on characteristics
# read the data
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("/content/clustervisitor.csv")
df.head(10)

# Perform segmentation based on characteristics (e.g., age groups)
cluster = {
    "Young" : df['Age'] <= 30,
    "Middle" : ((df['Age'] > 30) & (df['Age'] <= 50)),
    "Old" : df['Age'] > 50
}

```
### Output:
<img width="435" height="252" alt="image" src="https://github.com/user-attachments/assets/9597734b-4bcf-4004-b20b-6c7075f4b35f" />




### Visualization:
```python
# Create a list to store counts of visitors in each age group
visitor_counts = []
age_group_labels = []

# Count visitors in each age group
for group, age in cluster.items():
    visitor = df[age]
    print(f"The visitors in {group} age are")
    print(visitor)
    print(f"Visitor Count : {len(visitor)}")
    visitor_counts.append(len(visitor))
    age_group_labels.append(group)
    print("\n")
    
# Define age group labels and plot a bar chart
plt.figure(figsize=(8, 6))
plt.bar(age_group_labels, visitor_counts, color='skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitors')
plt.title('Visitor Distribution Across Age Groups')
plt.show()
```
### Output:
<img width="511" height="800" alt="image" src="https://github.com/user-attachments/assets/42f2418d-a36d-49ea-bff6-1dab5dfca006" />
<img width="477" height="144" alt="image" src="https://github.com/user-attachments/assets/7d197d47-44ac-4dcd-8ec4-7438d38d77fc" />
<img width="739" height="574" alt="image" src="https://github.com/user-attachments/assets/7a37922a-1b09-4044-bb52-a946c88657d2" />



### Result:
Thus we  Implementation of Cluster and Visitor Segmentation for Navigation patterns
