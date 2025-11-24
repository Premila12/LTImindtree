📝 Student Grading System – Python Project
📌 Project Overview
The Student Grading System is a modular Python application designed to read student records from CSV files, calculate their scores using flexible grading strategies, and produce detailed reports.
# 📝 Student Grading System – Python Project

## 📌 Project Description

The **Student Grading System** is a modular, well-structured Python application designed to read student records from a CSV file, process their scores through customizable grading strategies, and generate insightful reports.

Developed as part of hands-on Python training, this project demonstrates practical application of Python concepts like OOP, file handling, and data analysis in a clean, maintainable architecture.

Key highlights of the project include:
✔ Organized Python project structure (models, services, utils, data)
✔ Object-Oriented Programming with interchangeable grading strategies
✔ Robust CSV validation and secure data loading
✔ CLI-based user interaction via argparse
✔ Automatic export of results in JSON format
✔ Insightful report generation (grade distribution, pass rate, toppers)
✔ GitHub-ready project layout with README, .gitignore, and clean folder organization
This project demonstrates practical application of Python programming concepts, following **clean architecture principles** by separating models, services, and utilities, making the code easy to understand, extend, and maintain.

### This project showcases:
- ✔ **Proper Python project structure** (models, services, utils, data)
- ✔ **Object-Oriented Programming** with polymorphic grading strategies
- ✔ **CSV data validation** and safe loading
- ✔ **Customizable command-line interface** using argparse
- ✔ **Automatic JSON export** of final graded results
- ✔ **Useful report generation** (grade distribution, pass rate, toppers)
- ✔ **GitHub-ready layout** with README, .gitignore, and clean folder organization

'''📂 Project Structure

StudentGradingSystem/
│
├─ app.py
├─ README.md
│
├─ data/
│   ├─ students.csv
│   └─ results.json          (generated automatically)
│ ├─ students.csv
│ └─ results.json (auto-created after running)
│
├─ models/
│ ├─ init.py
│ └─ student.py
│
├─ services/
│ ├─ init.py
│ ├─ loader.py
│ ├─ analyzer.py
│ └─ reporter.py
│
└─ utils/
    ├─ __init__.py
    └─ grade_utils.py'''
    
├─ init.py
└─ grade_utils.py
```


---

🚀 Running the Project
Ensure Python 3.8+ is installed.

Default execution:

python app.py


Select grading strategy:


python app.py -s weighted


Custom CSV input and JSON output:

python app.py -i data/custom.csv -o output/results.json


See all CLI options:

python app.py --help


🎯 Features
✔ Load & validate CSV:

Confirms required columns exist

Skips rows with invalid data

Handles incorrect file paths

✔ Grading strategies with OOP:

SimpleAverageStrategy: Equal weight for assignments, quizzes, and exams

WeightedExamHeavyStrategy: Exam 60%, Assignment 20%, Quiz 20%

🎯 Features
✔ Load & validate CSV

Ensures required columns exist

Skips rows with invalid values

Catches wrong paths (file vs directory)

✔ Grading strategies using OOP

SimpleAverageStrategy: Equal weight for assignment, quiz, exam

WeightedExamHeavyStrategy: Exam = 60%, Assignment = 20%, Quiz = 20%

✔ Summary reporting:

Grade counts (A/B/C/D/F)

Average final score

Pass rate and failed student count

Top-performing students

✔ Save results to JSON:

Clean JSON output of all final scores and grades

🧩 Modules & Responsibilities

📘 models/student.py
Defines the Student dataclass with:

ID, Name

Assignment, Quiz, Exam scores

Final computed score

Letter grade
✔ Summary reporting

Displays:

Grade counts (A/B/C/D/F)

Average final score

Pass rate

Failed student count

Top performers

✔ Save final results to JSON

All final results (scores + grades) are stored in clean JSON format.

🧩 Modules & Responsibilities
📘 models/student.py

Defines the Student dataclass:

ID

Name

Assignment/quiz/exam scores

Computed final score

Letter grade

⚙️ services/loader.py
⚙️ services/loader.py

Handles CSV loading:

Validates columns

Converts CSV rows into Student objects

Handles file existence and directory errors

🧠 services/analyzer.py
Contains grading logic:

Abstract GradingStrategy base class

SimpleAverageStrategy and WeightedExamHeavyStrategy

apply_grading() computes final score and assigns letter grade

Validates columns

Converts rows → Student objects

Checks file existence

Handles wrong paths (directory instead of file)

🧠 services/analyzer.py

Contains:

GradingStrategy (abstract base class)

SimpleAverageStrategy

WeightedExamHeavyStrategy

apply_grading() to compute final score & letter grade

📊 services/reporter.py
Provides reporting and saving functions:

save_results_as_json()

print_summary()

print_top_students()

Outputs grade distribution, average score, pass rate, failed students, and top N performers

🔧 utils/grade_utils.py
Utility to convert numeric scores into letter grades:

A: 90+

B: 80+

C: 70+

D: 60+

F: <60

📑 Sample CSV (data/students.csv)

📊 services/reporter.py

Provides reporting functions:

save_results_as_json()

print_summary()

print_top_students()

Outputs include:

Grade distribution

Average final score

Pass rate

Failed students

Top N students

🔧 utils/grade_utils.py

Utility to convert numeric score → letter grade:

A (90+)

B (80+)

C (70+)

D (60+)

F (<60)

id,name,assignment,quiz,exam
1,Alice,85,90,88
2,Bob,70,65,72
3,Charlie,92,95,94
4,Drake,60,58,62
5,Edward,78,80,76


🖥 Example Console Output

===== Grade Summary =====
Grade A: 2 student(s)
Grade B: 2 student(s)
Grade C: 1 student(s)

Average final score: 81.25
Pass rate: 100.0% (5 / 5)
Failed students: 0

Top 3 students:
  1. Charlie - 93.67 [A]
  2. Alice - 87.67 [B]
  3. Edward - 78.00 [C]


📦 requirements.txt

# Standard library only
# Tested with Python 3.8+


🚫 .gitignore

__pycache__/
*.py[cod]
*$py.class

venv/
.env/

.vscode/

.DS_Store
Thumbs.db


👤 Author
K Premila Singha
GitHub: @Premila12



🎓 Acknowledgments
This project was inspired by hands-on Python training programs and developed to practice real-world application of Python OOP, file handling, and reporting.
