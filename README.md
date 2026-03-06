# 🎬 Netflix Shows Analysis

A comprehensive exploratory data analysis (EDA) of the Netflix titles dataset using Python and pandas. This project covers data loading, cleaning, transformation, selection/filtering, and key insights extracted from over 8,800 Netflix titles.

---

## 📁 Repository Structure

```
Netflix-Shows-Analysis/
├── Netflix-shows-analysis.ipynb   # Main analysis notebook
├── README.md
└── LICENSE
```

---

## 📊 Dataset

- **Source:** [Kaggle – Netflix Shows Dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **File:** `netflix_titles.csv`
- **Size:** 8,807 rows × 12 columns

### Columns

| Column | Description |
|---|---|
| `show_id` | Unique identifier for each title |
| `type` | Movie or TV Show |
| `title` | Title of the content |
| `director` | Director(s) of the content |
| `cast` | Cast members |
| `country` | Country of production |
| `date_added` | Date added to Netflix |
| `release_year` | Original release year |
| `rating` | Content rating (e.g., TV-MA, PG-13) |
| `duration` | Duration in minutes (Movies) or seasons (TV Shows) |
| `listed_in` | Genre categories |
| `description` | Brief description of the content |

---

## 🔧 Steps Performed

### 1. Data Loading & Inspection
- Loaded the dataset using `pandas`
- Inspected shape, dtypes, descriptive statistics, unique values, and null counts

### 2. Data Cleaning
- Filled missing values in `director`, `cast`, and `country` with their respective **mode**
- Converted `date_added` to `datetime` format
- Dropped rows with remaining nulls in `date_added`, `rating`, and `duration`
- Removed duplicate records
- Renamed `listed_in` → `genre`

### 3. Feature Engineering
- Extracted `year_added` and `month_added` from `date_added`
- Split `duration` into `numeric` (value) and `unit` (min / Season(s))
- Created a `categorize_data` column: "new" (release year ≥ 2020) / "old" (release year < 2020)

### 4. Data Selection & Filtering
- Filtered TV Shows and Movies separately
- Filtered titles released after 2015
- Sorted data by `release_year`, `date_added`, and `duration`

### 5. Exploratory Data Analysis (EDA)
- Total count of Movies vs. TV Shows: **6,126 Movies** and **2,664 TV Shows**
- Release year range: **1925 – 2021**
- Most common content rating: **TV-MA**
- Identified latest movies by title using `groupby`

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| Python 3.11 | Programming language |
| pandas | Data manipulation & analysis |
| datetime | Date parsing |
| Jupyter Notebook | Interactive development |

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas jupyter
```
### Run the Notebook
```bash
git clone https://github.com/HARSHIDS-4/Netflix-Shows-Analysis.git
cd Netflix-Shows-Analysis
jupyter notebook Netflix-shows-analysis.ipynb
```

> **Note:** The dataset (`netflix_titles.csv`) is sourced from Kaggle. Download it from [here](https://www.kaggle.com/datasets/shivamb/netflix-shows) and place it at `/kaggle/input/netflix-shows/netflix_titles.csv`, or update the file path in the notebook accordingly.

---

## 📈 Key Findings

- Netflix's catalog is dominated by **Movies (69.7%)** over TV Shows (30.3%)
- Content spans nearly **a century**, from 1925 to 2021
- The most frequent content rating is **TV-MA** (Mature Audiences)
- The majority of titles were added to Netflix between **2016 and 2021**

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙋‍♂️ Author

**HARSHIDS-4** — [GitHub Profile](https://github.com/HARSHIDS-4)
