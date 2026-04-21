# Student Academic Performance Analysis - EDA Dashboard Website

## Website Link: [https://student-performance-dashboard-ansh-yadav.netlify.app](https://student-data-analysis-ansh.netlify.app/)

A premium-quality, fully responsive website showcasing the Exploratory Data Analysis of student academic performance across Mathematics, Reading, and Writing.

---

## 🎯 Project Overview

This project presents a comprehensive EDA of 1,000 student records. The website features:

* **Interactive Visualizations**: 14+ charts created with Chart.js
* **Responsive Design**: Works on mobile, tablet, and desktop
* **Modern UI**: Dark theme with premium typography and grid layouts
* **Data Explorer**: Searchable, filterable, and sortable dataset
* **Lightweight Architecture**: Fully frontend-based (no backend required)

---

## 📊 Features

### Visualizations Included

**Basic Charts:**

* Average Score Trend (Line Chart)
* Grade Distribution (Donut Chart)
* Race / Ethnicity Distribution (Bar Chart)
* Parental Education Levels (Bar Chart)
* Score Distribution (Histogram)
* Average Score Spread (Box Plot)
* Math Score Trend (Area Chart)

**Advanced Charts:**

* Subject Scores by Gender (Grouped Bar Chart)
* Math vs Average Score (Scatter Plot)
* Gender vs Test Preparation (Cross-tab)
* Gender vs Lunch Type (Cross-tab)
* Test Preparation Impact Analysis
* Socioeconomic Impact (Lunch Type Analysis)
* Bubble Chart (Math vs Avg scaled by Reading)
* Correlation Heatmap
* Pairplot-style Multi-variable Analysis

---

## 📈 Key Insights Highlighted

* Reading and Writing scores outperform Mathematics overall
* Students who completed test preparation scored 5–10 points higher
* Strong socioeconomic impact based on lunch type (~11 point gap)
* Higher parental education correlates with higher student scores
* Balanced dataset with zero missing values

---

## 🛠️ Tech Stack

* **Frontend**: HTML5, CSS3, JavaScript (ES6+)
* **Charts**: Chart.js
* **Fonts**: Google Fonts (Syne, DM Sans, DM Mono)
* **Icons/UI**: Custom CSS (no external UI frameworks)
* **Deployment**: Netlify

---

## 🚀 Getting Started

### Option 1: Direct Open

Simply open `index.html` in any modern web browser.

```bash
# Navigate to project directory
cd student-performance-dashboard

# Open in browser (macOS)
open index.html

# Open in Windows
start index.html
```

---

### Option 2: Live Server (Recommended)

If using VS Code:

1. Right-click `index.html`
2. Click **Open with Live Server**

---

## 📁 Project Structure

```
student-performance-dashboard/
├── index.html          # Main dashboard file
├── README.md           # Project documentation
```

---

## 🎨 Design Features

* **Dark Theme**: Modern deep-color UI for better visualization
* **Grid Layouts**: Clean structured dashboard design
* **Typography**: Premium fonts (Syne, DM Sans, DM Mono)
* **Interactive UI**: Hover effects, transitions, dynamic charts
* **Dashboard Navigation**: Tab-based multi-section layout

---

## 📱 Responsive Breakpoints

* Mobile: < 768px
* Tablet: 768px – 1024px
* Desktop: > 1024px

---

## 🔧 Customization

### Changing Colors

Modify CSS variables in `index.html`:

```css
--accent: #6c63ff;
--bg: #0b0e1a;
--surface: #111527;
```

### Adding New Charts

1. Add dataset inside script section
2. Create new Chart.js instance
3. Add `<canvas>` element in HTML
4. Initialize chart in JS

---

## 📊 Data Source

The dataset contains 1,000 student records with features:

* Gender
* Race / Ethnicity
* Parental Education Level
* Lunch Type
* Test Preparation Status
* Mathematics Score
* Reading Score
* Writing Score
* Total Score
* Average Score
* Derived Grade Categories

---

## 👨‍💻 Author

* **Ansh Yadav**

---

Built for EDA Project | B.Tech

