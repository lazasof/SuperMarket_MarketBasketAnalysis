# SuperMarket_MarketBasketAnalysis
a first approach of a Market Basket Analysis for a chain of supermarkets in Greece consisiting of 416 Supermarkets.  
  
**Market Basket Analysis for Supermarket Chain**  
This repository contains code for performing market basket analysis on a dataset from a supermarket chain consisting of 416 supermarkets.   
The analysis involves processing transactional data to identify patterns of co-occurring items purchased together.   
Below are the steps outlined in the code:  
  
**Steps Performed in the Code:**    
**1. Data Loading and Preprocessing**  
The Python script begins by loading the transactional data from a CSV file and concatenating it into a single DataFrame.  
It then performs various data cleaning operations such as combining columns, dropping unnecessary columns, and filtering out rows with unique transaction IDs.  
  
**2. Data Sampling**  
The script further samples a subset of the preprocessed data to make the analysis computationally feasible.  
It randomly selects a specified number of rows from the DataFrame and filters out rows with unique transaction IDs.  
  

**3. Market Analysis Preparation**  
It prepares the data for market basket analysis by loading the sampled data, dropping irrelevant columns,   
and filtering out infrequent or irrelevant items from the dataset.  

  
**4. One-Hot Encoding & 5. Sparse Matrix Creation**  
This step involves the creation of a sparse matrix representation of the dataset to efficiently handle large datasets   
for association rule mining or one hot encoding, depends on usage.  
  

**6. Association Rule Mining**  
Using the FP-Growth algorithm, the script performs association rule mining to identify frequent itemsets and generate  
association rules based on a specified minimum support and confidence threshold.  
  
**7. Interpreting and Exporting Results**  
The generated association rules and frequent itemsets are interpreted and exported as CSV files. Additionally,  
the code provides functionality to map IDs to corresponding product names based on an auxiliary dataset containing item information.  


**Files Generated:**  

  
**frequent_itemsets.csv:** Contains the frequent itemsets generated from the dataset.  
**rules.csv:** Contains the association rules extracted from the dataset.  
**finalrules.csv:** Enhanced version of association rules with product names mapped.  
**final_frequentitemsets.csv:** Enhanced version of frequent itemsets with product names mapped.  


    
**How to Use:**  

  
**Data Preparation:** Ensure your transactional data is in CSV format and update the file paths in the provided Python script to point to your dataset.  
**Adjust Parameters:** Modify parameters like chunk sizes, minimum support, and confidence thresholds according to your dataset size and analysis requirements.  
**Run the Script:** Execute the Python script to perform market basket analysis.  
**Interpret Results:** Check the generated CSV files for frequent itemsets and association rules. Explore the relationships between items and their co-occurrences.  
