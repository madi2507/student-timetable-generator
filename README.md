# Student Timetable Generator

A hybrid AI system designed to help students manage their academic workload by generating study plans and assessing study-related risk.

## Overview

The Student Timetable Generator combines search algorithms, rule-based reasoning, and machine learning to support students in planning their study time.

The user provides information about their academic workload, available study time, confidence, and stress level. The system then generates a study plan and assesses the potential study-related risk.

### User Inputs

The system uses information such as:

- Task name
- Required study hours
- Deadline / days remaining
- Available study days
- Available study time
- Confidence level (1–3)
- Stress level (1–3)

### System Outputs

The system produces:

- A weekly study plan
- A risk level: LOW, MEDIUM, or HIGH
- Machine-learning prediction
- Rule-based prediction
- Explanations for the assessment
- Warnings when there is not enough available study time

## How It Works

The system combines three main approaches.

### 1. Search-Based Planner

Two search approaches are implemented and compared:

- **BFS (Breadth-First Search)** — assigns study time step by step based on the order of tasks.
- **Greedy Algorithm** — prioritises tasks using their deadlines and required study hours.

The Greedy approach is used as the main scheduling method.

### 2. Rule-Based System

A rule-based system evaluates factors such as:

- Task size
- Deadline
- Confidence level
- Stress level

Based on these factors, the system generates a risk assessment and an explanation of the decision.

### 3. Machine Learning

A **Logistic Regression** model is used for binary risk prediction.

The model uses features including:

- Task hours
- Days remaining
- Confidence
- Stress

The model is trained using a small synthetic dataset with an 80/20 train-test split.

## Final Decision

The system combines the machine-learning prediction with the rule-based assessment to produce the final risk level.

The generated results include:

- Study timetable
- BFS vs Greedy comparison
- Machine-learning prediction
- Rule-based prediction
- Final risk level
- Explanations
- Study-time warnings

## How to Run

1. Download or clone this repository.
2. Make sure both `student-timetable-generator.ipynb` and `student_data.csv` are available in the same folder.
3. Open `student-timetable-generator.ipynb` using Jupyter Notebook, JupyterLab, or Google Colab.
4. Run the notebook cells from top to bottom.
5. Enter your own study information when prompted, including:
   - Task name
   - Required study hours
   - Deadline / days remaining
   - Available study days
   - Available study time
   - Confidence level (1–3)
   - Stress level (1–3)
6. The system will generate a study plan and assess the study-related risk based on the information provided.

### Dataset

The `student_data.csv` file is required for the machine-learning component of the project.

**Note:** The dataset contains synthetic data created for this project and does not contain real student data.

## Testing

The system was tested using different scenarios, including:

- High workload with short deadlines and high stress
- Lower workload with sufficient available study time
- Insufficient available study time
- Invalid confidence and stress inputs

## Technologies

- Python
- Jupyter Notebook
- Scikit-learn
- Logistic Regression
- BFS
- Greedy Search
- Rule-Based Reasoning
- CSV Dataset

## Project Files

- `student-timetable-generator.ipynb` — main project implementation and interactive system.
- `student_data.csv` — synthetic dataset used by the machine-learning component.
- `Readme_student_timetable.docx` — detailed project report.

## Limitations

The machine-learning model was trained on a small and simple synthetic dataset. Therefore, its predictions should be treated as guidance rather than exact assessments.

The project is intended as an academic demonstration of combining search algorithms, rule-based reasoning, and machine learning for student study planning.

## Author

**Madina**
