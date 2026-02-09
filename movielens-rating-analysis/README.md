## MovieLens Rating Distribution Analysis
`I request to see the jupyter notebook file so get the proper clarity of the project`

---

### 📌 Project Overview

This project analyzes the **MovieLens 10M dataset** to study **user rating behavior** and **movie popularity patterns**.

Rather than treating this as a simple assignment, the dataset is approached as a **real-world analytics problem**, emphasizing:

- Large-scale data handling  
- Performance considerations  
- Clear interpretation of results  

The project includes **data preprocessing, sorting, histogram analysis, and performance benchmarking** using Python.

---

###  📊 Dataset

**Source:** MovieLens 10M Dataset  
**Primary File:** `ratings.dat`

### Data Format
`UserID :: MovieID :: Rating :: Timestampt`

Due to the dataset’s size (**~10 million rows**), careful handling was required to ensure **performance, efficiency, and reproducibility**.

---

### Tools & Technologies

- **Python**
- **Jupyter Notebook**
- **NumPy**
- **Matplotlib**
- **Dictionaries & Custom Algorithms**
- **File-based Data Processing**

#### 📂 Repository Structure

data/ → Processed dataset partitions -> the dataset was too large so I have put a link to download dataset online
notebook/ → Full analysis workflow

---

### 🔹 Step 1: Dataset Splitting

The original ratings file was divided into **five nearly equal partitions** to:

- Improve processing efficiency  
- Enable modular analysis  
- Simulate real-world, partitioned data workflows  

A **custom Python script** reads the file **line-by-line**, preventing memory overload.

---

### 🔹 Step 2: Sorting by Rating

Two sorting strategies were implemented and benchmarked.

#### Manual Sorting
- Custom **Insertion Sort**
- Applied to a subset of the data
- Demonstrates algorithmic understanding

#### Built-in Sorting
- Python’s optimized `sorted()` function
- Applied to the full dataset
- Used for performance benchmarking

Execution time for both methods was recorded and compared.

---

### 🔹 Step 3: Rating Distribution Histogram

A histogram was generated to visualize overall user rating behavior.

**Key Details:**
- Rating scale: **0.5 – 5.0**
- Histogram computation time measured using **NumPy**
- Plot rendering time excluded for fair benchmarking

---

### 🔹 Step 4: Movie Popularity Analysis

The total number of ratings per movie was computed.

#### Observations:
- Most movies receive relatively few ratings  
- A small subset dominates user attention  
- Distribution follows a **long-tail pattern**, common in real-world platforms  

---

### 🔹 Step 5: Low vs High Rating Comparison

Ratings were grouped into two categories:

| Category | Ratings |
|--------|---------|
| **Low Ratings** | 0.5, 1.0, 1.5 |
| **High Ratings** | 4.0, 4.5, 5.0 |

Separate histograms were created to analyze user sentiment.

**Result:**  
Users show a strong **positive bias**, with high ratings far more common than low ratings.

---

### 📈 Key Insights

- User ratings are skewed toward higher values  
- Movie popularity follows a long-tail distribution  
- Built-in algorithms vastly outperform manual sorting  
- Separating computation from visualization improves performance analysis  

---

---

### Why This Project Matters

This project demonstrates:

- Ability to work with **large-scale datasets**
- **Performance-conscious** coding practices
- Strong analytical reasoning
- Professional project organization
- Reproducible data analysis workflows

---

## These are the only things I used for this work as we just got to how to handle the data 
`numpy
matplotlib` 


