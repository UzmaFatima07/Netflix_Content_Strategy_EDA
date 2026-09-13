# 🎬 Netflix Content Strategy — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)

## 📌 Project Overview

This project performs an **end-to-end Exploratory Data Analysis (EDA)** of the Netflix Movies and TV Shows dataset to understand the platform's content library, identify distribution patterns, analyze content growth over time, and uncover regional and content-related trends.

The analysis focuses not only on visualizing the dataset but also on transforming raw data into meaningful insights that can help understand **Netflix's content strategy**.

The project covers the complete EDA workflow:

```text
Raw Dataset
     ↓
Data Understanding
     ↓
Data Cleaning
     ↓
Missing Value Analysis
     ↓
Data Transformation
     ↓
Feature Engineering
     ↓
Univariate Analysis
     ↓
Bivariate / Multivariate Analysis
     ↓
Visualization
     ↓
Business Insights
```

---

# 🎯 Objectives

The main objectives of this project were to:

* Understand the overall composition of Netflix's content library.
* Compare **Movies vs. TV Shows**.
* Analyze Netflix's content growth over the years.
* Identify trends in content additions.
* Examine content distribution across countries and regions.
* Analyze ratings and audience categories.
* Explore genre distribution and popularity.
* Investigate the relationship between release year and content addition.
* Identify missing-data patterns and handle them appropriately.
* Engineer meaningful features for deeper analysis.
* Extract business-oriented insights from the data.

---

# 📊 Dataset

The project uses the **Netflix Movies and TV Shows dataset**, containing information about titles available on Netflix.

The dataset includes attributes such as:

| Feature        | Description                                    |
| -------------- | ---------------------------------------------- |
| `show_id`      | Unique identifier for each title               |
| `type`         | Movie or TV Show                               |
| `title`        | Title name                                     |
| `director`     | Director of the title                          |
| `cast`         | Main cast members                              |
| `country`      | Country or countries associated with the title |
| `date_added`   | Date the title was added to Netflix            |
| `release_year` | Original release year                          |
| `rating`       | Content rating                                 |
| `duration`     | Movie duration or number of TV seasons         |
| `listed_in`    | Genre/category information                     |
| `description`  | Title description                              |

The dataset contains **8,800+ Netflix titles**, making it suitable for exploring large-scale content distribution and catalog trends.

---

# 🧹 Data Cleaning & Preprocessing

Before performing analysis, the dataset was examined for quality issues and inconsistencies.

### Missing Value Analysis

Missing values were investigated across important columns such as:

* Director
* Cast
* Country
* Date Added
* Rating
* Duration

Rather than blindly filling every missing value, the missingness was considered in the context of the corresponding feature.

### Data Cleaning Tasks

The analysis included:

* Identifying missing values.
* Handling missing categorical information.
* Cleaning date-related fields.
* Converting columns into appropriate data types.
* Checking temporal consistency.
* Removing or handling problematic records where necessary.
* Preparing categorical and numerical variables for analysis.

---

# 🛠️ Feature Engineering

Additional features were created to make the dataset more useful for analysis.

### `year_added`

Extracted the year from the `date_added` field to analyze Netflix's content addition trends over time.

### `content_age`

Created a feature representing the age of content based on its release year and the year it was added to Netflix.

This helped investigate questions such as:

> Does Netflix primarily add newly released content, or does its library also contain older titles?

---

# 🔍 Exploratory Data Analysis

The project uses both **univariate** and **multivariate** analysis to understand the Netflix catalog.

## 1. Movies vs. TV Shows

Analyzed the overall distribution of:

* Movies
* TV Shows

This helps understand the dominant content format in Netflix's catalog.

---

## 2. Content Growth Over Time

Analyzed how Netflix's content library changed across different years.

The analysis examined:

* Number of titles by release year.
* Number of titles added to Netflix over time.
* Growth patterns in the catalog.
* Changes in content availability across different periods.

This provides a view of how Netflix's content strategy evolved as the platform expanded.

---

## 3. Genre Analysis

The `listed_in` column contains multiple genres/categories for many titles.

Genre information was analyzed to understand:

* Most common content categories.
* Distribution of genres across the platform.
* Differences between Movies and TV Shows.
* Content preferences represented in the catalog.

---

## 4. Country & Regional Analysis

The `country` field was analyzed to understand Netflix's global content distribution.

Questions explored include:

* Which countries contribute the most titles?
* How geographically diverse is Netflix's catalog?
* Which regions have stronger representation?
* How does content distribution vary internationally?

---

## 5. Rating Analysis

Content ratings were analyzed to understand the intended audience of Netflix titles.

The analysis examined:

* Most common ratings.
* Distribution of ratings.
* Differences between Movies and TV Shows.
* Audience targeting patterns.

---

## 6. Content Duration Analysis

The `duration` column contains different formats for Movies and TV Shows.

For example:

```text
Movies → minutes
TV Shows → number of seasons
```

Therefore, duration was considered separately for different content types to avoid misleading comparisons.

Visualizations such as box plots were used to examine the distribution and identify potential outliers.

---

## 7. Text & Description Analysis

Text-based analysis was also performed using title/description information.

A **WordCloud** was created to identify frequently occurring words and themes within the available textual information.

This provides an additional qualitative perspective on Netflix's catalog.

---

# 📈 Visualizations

The analysis includes multiple visualization techniques to communicate patterns effectively.

### Visualization techniques used

* Bar charts
* Count plots
* Histograms
* Box plots
* Pie charts
* Line plots
* Distribution plots
* WordClouds
* Multivariate visualizations

These visualizations were used to transform raw numerical and categorical data into interpretable insights.

---

# 💡 Key Analytical Insights

The analysis provides several useful observations about Netflix's content catalog.

### 📺 Content Type

Netflix's catalog contains both Movies and TV Shows, with Movies representing a substantial portion of the available titles.

Understanding this split is useful when evaluating Netflix's overall content strategy.

### 📈 Library Growth

The analysis reveals a significant increase in Netflix's content additions during the later years represented in the dataset.

This indicates the platform's rapid expansion of its content catalog.

### 🌍 Global Content

Netflix's catalog is geographically diverse, with content associated with multiple countries.

This reflects the importance of international and regional content in a global streaming platform.

### 🎭 Genre Diversity

The catalog contains a broad range of genres, demonstrating Netflix's strategy of serving different audience segments rather than relying on a single content category.

### ⭐ Audience Targeting

The distribution of ratings provides insight into the types of audiences represented within Netflix's catalog and the platform's focus on different age groups.

### ⏳ Content Age

The engineered `content_age` feature helps distinguish between newer releases and older content added to Netflix, providing a more useful perspective than looking at release year alone.

---

# 🧠 Business Perspective

The purpose of this project was not simply to create charts.

The analysis demonstrates how exploratory data analysis can support questions related to **content strategy and business decision-making**.

For example:

### Content Acquisition

Understanding the age and origin of content can help identify whether a platform is relying more heavily on new releases or maintaining a large library of older titles.

### Regional Strategy

Country-level analysis can help identify regions with strong content representation and potential opportunities for further localization.

### Audience Segmentation

Rating and genre distributions provide insight into the different audience segments being served by the platform.

### Catalog Planning

Understanding genre and content-type trends can help identify areas where a streaming platform may be overrepresented or underrepresented.

---

# 🛠️ Tech Stack

### Programming Language

* Python

### Data Analysis

* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn
* WordCloud

### Development Environment

* Jupyter Notebook

---

# 📁 Repository Structure

```text
Netflix_Content_Strategy_EDA/
│
├── NetflixContentStrategyEDA.ipynb
│
└── README.md
```

---

# 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/UzmaFatima07/Netflix_Content_Strategy_EDA.git
```

### 2. Navigate to the project directory

```bash
cd Netflix_Content_Strategy_EDA
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn wordcloud jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open

```text
NetflixContentStrategyEDA.ipynb
```

Run the notebook cells sequentially to reproduce the analysis.

> **Note:** If the notebook uses an external dataset path, update the dataset path according to your local environment.

---

# 📚 Skills Demonstrated

Through this project, I practiced:

* Python for Data Analysis
* Pandas Data Manipulation
* NumPy
* Data Cleaning
* Missing Value Analysis
* Feature Engineering
* Exploratory Data Analysis
* Univariate Analysis
* Bivariate Analysis
* Multivariate Analysis
* Data Visualization
* Categorical Data Analysis
* Temporal Analysis
* Text-Based Visualization
* Business-Oriented Data Interpretation

---

# 🔎 Key Takeaway

This project strengthened my understanding that **EDA is more than creating visualizations**.

A strong analysis requires:

```text
Understand the Data
       ↓
Identify Data Quality Issues
       ↓
Clean the Data
       ↓
Engineer Useful Features
       ↓
Explore Patterns
       ↓
Visualize Findings
       ↓
Interpret the Results
       ↓
Translate Findings into Business Insights
```

The project helped me develop a more structured approach to analyzing real-world datasets and communicating findings in a way that can support data-driven decision-making.

---

# 👩‍💻 Author

**Uzma Fatima**

Engineering Student | Aspiring Data Analyst | Machine Learning Enthusiast

### GitHub

[UzmaFatima07](https://github.com/UzmaFatima07)

---

⭐ If you find this project useful, feel free to explore the notebook and follow my data analytics journey.
