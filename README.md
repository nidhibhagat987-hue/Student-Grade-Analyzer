# Student Grade Analyzer

Author  : Nidhi Bhagat
College : Birla Institute of Technology, Mesra
Tool    : Google Colab | Python 3

---

## About

Student Grade Analyzer is a Python-based academic performance analysis tool
built for a class of 20 students across 6 core Computer Science subjects.
It computes statistics, ranks students, assigns letter grades, generates
publication-quality charts, and exports a comprehensive PDF report.

---

## Objectives

1. Load and validate a structured student dataset (20 students, 6 subjects)
2. Compute subject-wise and overall academic performance statistics
3. Rank all students and assign letter grades using a standard GPA scale
4. Identify top performers, at-risk students, and subject difficulty levels
5. Detect pass/fail outcomes across all subjects and compute class-level KPIs
6. Produce 6 publication-quality visualizations
7. Export a structured PDF report summarizing all findings and charts

---

## Subjects Covered

- Data Structures
- Object Oriented Programming (OOP)
- Database Management Systems (DBMS)
- Operating Systems
- Computer Networks
- Software Engineering

---

## Features

- Subject-wise statistics: mean, max, min, standard deviation, pass rate
- Student ranking with letter grades (A+ to F) and GPA values
- Pass/Fail detection based on performance across all subjects
- Class-level KPIs: class average, top ranker, hardest and easiest subject
- 6 visualizations: violin plot, box plot, heatmap, radar chart, pie chart, bar chart
- Auto-generated multi-page PDF report with tables, charts, and conclusions

---

## Grading Scale

| Average Score | Grade | GPA  |
|---------------|-------|------|
| 90 and above  | A+    | 10.0 |
| 80 to 89      | A     | 9.0  |
| 70 to 79      | B+    | 8.0  |
| 60 to 69      | B     | 7.0  |
| 50 to 59      | C     | 6.0  |
| 40 to 49      | D     | 5.0  |
| Below 40      | F     | 0.0  |

Pass condition: Student must score 40 or above in ALL subjects.

---

## Visualizations Generated

1. Chart 1 - Score Distribution: Violin plot and box plot for all subjects
2. Chart 2 - Student Rankings: Horizontal bar chart ranked by average score
3. Chart 3 - Score Heatmap: Subject-wise heatmap for all 20 students
4. Chart 4 - Grade Overview: Grade distribution pie chart and pass/fail donut chart
5. Chart 5 - Subject Difficulty: Mean with standard deviation and subject pass rates
6. Chart 6 - Radar Chart: Top 3 vs Bottom 3 students across all subjects

---

## Output Files

- chart1_distribution.png
- chart2_rankings.png
- chart3_heatmap.png
- chart4_grades_pie.png
- chart5_difficulty.png
- chart6_radar.png
- Student_Grade_Analyzer_Report.pdf

---

## Requirements

Install dependencies using:

    pip install pandas numpy matplotlib fpdf2

Or if running on Google Colab, the script installs fpdf2 automatically.

---

## How to Run

Option 1 - Google Colab (Recommended):
1. Open Google Colab at colab.research.google.com
2. Create a new notebook
3. Paste the entire script into a single cell
4. Press Shift + Enter to run
5. All charts and the PDF report will be generated automatically

Option 2 - Local Python:
1. Install Python 3.8 or above
2. Install dependencies: pip install pandas numpy matplotlib fpdf2
3. Run the script: python student_grade_analyzer.py
4. Output files will be saved in the same directory

---

## Project Structure

    Student-Grade-Analyzer/
    |
    |-- student_grade_analyzer.py     Main Python script
    |-- README.md                     Project documentation
    |-- requirements.txt              Python dependencies

---

## Technologies Used

| Category          | Tool / Library                              |
|-------------------|---------------------------------------------|
| Language          | Python 3                                    |
| Environment       | Google Colab                                |
| Data Handling     | Pandas, NumPy                               |
| Visualization     | Matplotlib                                  |
| PDF Generation    | FPDF2                                       |
| Concepts Applied  | Data analysis, statistics, visualization    |

---

## Known Fixes Applied

1. AttributeError on std() - Fixed by replacing df[s].std().round(2) with
   round(df[s].std(), 2) since std() returns a plain Python float scalar
   which does not support the .round() method.

2. FPDFUnicodeEncodingException - Fixed by adding a sanitize() function that
   replaces all non-Latin-1 characters such as em dashes and curly quotes
   with plain ASCII equivalents before passing any string to FPDF.

---

## Sample Output Summary

- Class Average    : 73.5 / 100
- Top Ranker       : Ananya Singh
- Students Passed  : 17 / 20
- Students Failed  : 3 / 20
- Pass Rate        : 85%
- Hardest Subject  : Computer Networks
- Easiest Subject  : Software Engineering

---

## Author Note

This project was built as part of an academic data analysis exercise at
Birla Institute of Technology, Mesra. It demonstrates the use of Python
for real-world data processing, statistical analysis, and automated
report generation.

---

## License

This project is open for academic and educational use.
