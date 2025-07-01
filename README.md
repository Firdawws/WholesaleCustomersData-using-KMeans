# **Wholesale-Customers-Data-Segmentation-Using K-Means**

## ** Table of Contents**  
1. [Overview](Overview)  
2. [Dataset](#The_Dataset)  
3. [Project Workflow](#Project_Workflow)  
   - [Data Preprocessing](#part_1_Data_preprocessing_and_EDA)  
   - [Optimal Number of Clusters](#Part_2_Optimal_Number_of_Clusters)
   - [Apply KMeans with Optimal K ](#Part_3_Apply_KMeans_with_Optimal_K)
4. [Project Structure](#Project_Structure)  
5. [Requirements](#Requirements)  


---
## Overview
This project applies KMeans clustering to segment customers in the Wholesale Customers Dataset based on their annual spending on six product categories. The aim is to uncover natural groupings in customer behavior and develop data-driven marketing strategies for each group.

## **📊 The Dataset**  
The dataset is sourced from the **UCI Machine Learning Repository**:  
🔗 [Wholesale Customers Data](https://archive.ics.uci.edu/dataset/292/wholesale+customers)  
The dataset contains **annual spending** data(in monetary units) of wholesale customers

### ** Features:**  
- **Channel**: Type of customer (Hotel/Restaurant/Café or Retailer).  
- **Region**: Geographic region of the customer.  
- **Fresh**: Annual spending on fresh products.  
- **Milk**: Annual spending on milk products.  
- **Grocery**: Annual spending on grocery items.  
- **Frozen**: Annual spending on frozen products.  
- **Detergents_Paper**: Annual spending on detergents and paper products.  
- **Delicatessen**: Annual spending on delicatessen items.  

---
##  Project Workflow**
### **part 1.Data preprocessing and EDA**
✔️Load dataset and view the data.

✔️Handle missing values,duplicates (if any).  

✔️Visualize the data using histograms, scatter and boxplots plots.  

✔️Identify correlations between features using Heatmap

✔️Detect and treat outliers using boxplots.  

✔️Normalize the data for uniform scaling. 

### Part 2: Optimal Number of Clusters
- Used **KMeans** clustering for values of `K` from 2 to 10
- Evaluated each `K` using:
  - **Inertia (Elbow Method)**
  - **Silhouette Score**
- Selected the best `K` based on both metrics

### Part 3: Apply KMeans with Optimal K
- Fit final KMeans model with optimal `K`
- Assigned each customer to a cluster
- Added cluster labels to the dataset

### Part 4: Cluster Profiling
- Calculated mean annual spending for each cluster
- Interpreted customer behavior in each group
- Proposed personalized marketing strategies


## **Project_Structure**  
```bash
📁 Wholesale-Customers-data-using--KMeans
│── 📁 data                  # Dataset folder  
│   ├── Wholesale customers data.csv   
│── 📊 CustomerSegmentation using K-Means.ipynb   
│── 📄 README.md            # Project Documentation                    
```


### **Requirements**  
you can run this project using any of the following options:
** option 1: Install Python libraries locally**
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

Then run the project using your preferred code editor e.g pycharm,VS Code or terminal 

** Option 2: Use Jupyter Notebook via Anaconda**

** Steps:**
- Download and install Anaconda.
- Open Anaconda Navigator and launch Jupyter Notebook.
- Open the .ipynb file and run the code cells.

Anaconda comes with all required libraries pre-installed.

**Option 3: Use Google Colab (No Installation Needed)**

**You can also run this notebook in your browser using Google Colab.**
**💡 Steps:**
- Upload the .ipynb file to Google Colab.
- Make sure to upload the dataset (.csv file) as well.
- Run the notebook
