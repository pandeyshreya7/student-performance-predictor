
# 🎓 Student Performance Predictor

> A beginner-friendly Machine Learning project built with Python and Scikit-learn.
> Predicts a student's final exam score based on study habits and past performance.

---

## 📌 What Does This Project Do?

Given three simple inputs about a student:
- 📚 **Study Hours** — how many hours per day they study
- 🏫 **Attendance** — their class attendance percentage
- 📝 **Previous Scores** — their score in the last exam

…the model **predicts their final exam score** using a Decision Tree — a machine learning algorithm that learns patterns from historical data.

---

## 🗂️ Project Structure

```
student-performance-predictor/
│
├── data/
│   └── student_data.csv      ← Sample dataset (50 students)
│
├── notebook.ipynb            ← Main project notebook (step-by-step)
├── requirements.txt          ← Python packages needed
└── README.md                 ← You are here!
```

---

## ⚙️ Setup Instructions

### Step 1: Clone or Download the Project
```bash
git clone https://github.com/your-username/student-performance-predictor.git
cd student-performance-predictor
```

### Step 2: (Optional but Recommended) Create a Virtual Environment
```bash
# Create a virtual environment
python -m venv venv

# Activate it:
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate
```

### Step 3: Install Required Libraries
```bash
pip install -r requirements.txt
```

### Step 4: Launch the Notebook
```bash
jupyter notebook notebook.ipynb
```

Your browser will open. Click **Run All** or run cells one by one!

---

## 🧪 Requirements

| Library | Version | Purpose |
|---------|---------|---------|
| pandas | 2.1.4 | Load and clean data |
| numpy | 1.26.4 | Math operations |
| matplotlib | 3.8.2 | Draw graphs |
| seaborn | 0.13.2 | Prettier graphs |
| scikit-learn | 1.4.0 | Machine learning |
| notebook | 7.1.0 | Run Jupyter notebooks |

---

## 📊 Dataset

The dataset (`data/student_data.csv`) contains **50 synthetic student records**:

| Column | Description | Range |
|--------|-------------|-------|
| `student_id` | Unique student number | 1–50 |
| `study_hours` | Daily study hours | 0.5–8.0 |
| `attendance` | Attendance percentage | 40–100 |
| `previous_scores` | Last exam score | 30–96 |
| `final_score` | Final exam score (target) | 33–98 |

---

## 🤖 How the Model Works

We use a **Decision Tree Regressor** — here's a simple analogy:

> Imagine a tree of yes/no questions:
> - "Does the student study more than 5 hours?" → Yes
>   - "Is attendance above 85%?" → Yes
>     - → Predict score: **91**

The model learns these decision rules **automatically** from the training data!

### Why Decision Tree?
- ✅ Easy to understand (you can visualize it!)
- ✅ No need to scale/normalize features
- ✅ Works well for small datasets
- ✅ Great for learning ML fundamentals

---

## 📈 What You'll See in the Notebook

1. **Data Loading** — Read the CSV into a Pandas DataFrame
2. **Data Exploration** — Summary statistics, shape, data types
3. **Data Cleaning** — Check for missing values and duplicates
4. **Visualizations** — 4 graphs including scatter plots and a heatmap
5. **Model Training** — Train a Decision Tree on 80% of the data
6. **Tree Visualization** — See the actual decision tree drawn out
7. **Evaluation** — MAE score with plain-English explanation
8. **Prediction** — Predict scores for 3 example students + your own input

---

## 📏 Model Evaluation

| Metric | What It Means |
|--------|---------------|
| **MAE (Mean Absolute Error)** | Average number of points the prediction is off by |
| **R² Score** | How much variation in scores the model explains (1.0 = perfect) |

**Example:** If MAE = 2.5, and a student's real score is 80, the model predicts between 77.5 and 82.5. That's accurate!

---

## 🔮 Make Your Own Prediction

Inside the notebook, you can enter any student's data:

```python
predict_score(
    study_hours=4.0,      # Hours studied per day
    attendance=85,        # % of classes attended
    previous_score=74     # Score in the last exam
)
# Output: 78.0
```

---

## 🚀 Ideas to Extend This Project

- Add more features: `sleep_hours`, `extracurricular_activities`, `assignments_done`
- Try other models: `LinearRegression`, `RandomForestRegressor`
- Build a simple web app with **Streamlit** to make it interactive
- Collect real anonymized student data and retrain
- Add cross-validation for more reliable accuracy measurement

---

## 📚 Concepts Covered

| Concept | Explanation |
|---------|-------------|
| DataFrame | A table-like data structure in Pandas |
| Features (X) | Input columns used to make predictions |
| Target (y) | The column we want to predict |
| Training set | 80% of data the model learns from |
| Test set | 20% of data used to evaluate accuracy |
| Overfitting | When a model memorizes training data but fails on new data |
| MAE | Average prediction error in the same unit as the target |

---

## 🙌 Acknowledgements

- Dataset: Synthetically generated for educational purposes
- Libraries: [Scikit-learn](https://scikit-learn.org/), [Pandas](https://pandas.pydata.org/), [Matplotlib](https://matplotlib.org/), [Seaborn](https://seaborn.pydata.org/)
- Great starting point for anyone learning ML!

---

## 📄 License

This project is open-source and free to use for learning purposes.

---

*Built with ❤️ for beginner ML learners*
=======
