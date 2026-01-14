# Seoul Senior Welfare Facility Gap Analysis Project

## 📊 Project Overview
This data analysis project analyzes the distribution of senior population and welfare facility status across Seoul's 25 autonomous districts to visualize **supply-demand imbalances** and **identify service gaps**.

### 🎯 Key Findings
- **Gangdong District** identified as Seoul's only senior welfare facility service gap
- **Supply imbalance** issue discovered: high senior population but insufficient facilities
- Service gaps determined by falling below 80% of Seoul's average

---

## 🔍 Analysis Objectives
1. Assess senior population status by autonomous district
2. Analyze senior welfare facility supply status
3. Identify service gaps through calculation of facilities per 1,000 seniors
4. Conduct cross-analysis by facility type (medical/residential/home care/leisure)

---

## 📈 Generated Dashboards

### 1️⃣ Senior Population TOP 5 vs BOTTOM 5
- **Top 5 Districts**: Songpa, Gangseo, Nowon, Eunpyeong, Gangdong
- **Bottom 5 Districts**: Seongdong, Geumcheon, Yongsan, Jongno, Jung
- 💡 **Insight**: All three Gangnam-area districts (Songpa, Gangdong, Gangnam) ranked in top tier, as expected

### 2️⃣ Facility Count TOP 5 vs BOTTOM 5
- **Top 5 Districts**: Nowon, Gangseo, Jungnang, Yangcheon, Songpa
- **Bottom 5 Districts**: Gwangjin, Geumcheon, Yongsan, Jongno, Jung
- 💡 **Insight**: Gangnam-area districts ranked in bottom tier for facilities—opposite of expectations!

### 3️⃣ Facilities per 1,000 Seniors (All 25 Districts)
- **Seoul Average**: 3.85 facilities
- **Threshold** (Average × 0.8): 3.08 facilities
- 🚨 **Service Gap**: Only Gangdong District falls below threshold (3.09 facilities)

### 4️⃣ Heatmap - District × Facility Type Cross-Analysis
- Visualized distribution by medical facilities, residential facilities, home care facilities, and leisure facilities
- 💡 **Insight**: Gangdong District falls below average across all facility types

---

## 🛠️ Technology Stack

### Data Analysis
- **Python 3.x**
- **pandas**: Data preprocessing and analysis
- **numpy**: Numerical computation

### Visualization
- **Plotly**: Interactive dashboard generation
  - `plotly.graph_objects`: Detailed chart customization
  - `plotly.subplots`: Multiple chart layout
  - Various visualization types including heatmaps and bar charts

### Development Environment
- **Google Colab**: Cloud-based development and collaboration

---

## 📂 Project Structure

```
Senior_Project/
├── 노인프로젝트_최종_코드.ipynb    # Main analysis notebook
├── 분석데이터_완전판.csv           # Analysis data (including facility types)
├── README.md                      # Project documentation (Korean)
├── README_EN.md                   # Project documentation (English)
└── outputs/                       # Generated HTML dashboard files
    ├── 대시보드1_노인인구_TOP5_BOTTOM5.html
    ├── 대시보드2_시설수_TOP5_BOTTOM5.html
    ├── 대시보드3_노인1000명당시설수_전체.html
    └── 대시보드4_히트맵_자치구_시설유형.html
```

---

## 🚀 How to Run

### 1. Run in Google Colab
```
1. Access Google Colab: https://colab.research.google.com/
2. Upload 노인프로젝트_최종_코드.ipynb
3. Prepare data file '분석데이터_완전판.csv'
4. Execute cells in order (Shift + Enter)
```

### 2. Run in Local Environment
```bash
# Install required libraries
pip install pandas numpy plotly

# Launch Jupyter Notebook
jupyter notebook 노인프로젝트_최종_코드.ipynb
```

---

## 📊 Data Structure

### Input Data (`분석데이터_완전판.csv`)
| Column Name | Description |
|-------------|-------------|
| `자치구명` | Names of Seoul's 25 autonomous districts |
| `65세이상인구` | Senior population aged 65+ by district |
| `시설수` | Total number of senior welfare facilities by district |
| `의료복지시설` | Number of medical welfare facilities |
| `주거복지시설` | Number of residential support facilities |
| `재가복지시설` | Number of home care service facilities |
| `여가복지시설` | Number of leisure activity facilities |
| `노인1000명당시설수` | Facilities per 1,000 seniors (key metric) |

---

## 🎨 Visualization Features

### Design System
- **Color Coding**: 
  - 🔴 Red (`#ef4444`): Bottom tier/below threshold
  - 🔵 Blue (`#3b82f6`): Top tier/above threshold
  - 🟢 Green (`#10b981`): Seoul average line
- **Font**: Malgun Gothic (optimized for Korean readability)
- **Interactive**: Detailed information displayed on mouse hover

### Key Features
- Comparative analysis of top/bottom 5 districts
- Visualization of Seoul average line and threshold
- Highlighting of Gangdong District service gap
- Saved as HTML files for use in presentations

---

## 📌 Key Insights

### ✅ As Expected
- Gangnam-area districts (Songpa, Gangdong, Gangnam) ranked in top tier for senior population
- Senior population concentrated in densely populated areas

### ⚠️ Contrary to Expectations
- Gangnam-area districts ranked in bottom tier for facility count
- **Supply imbalance**: High senior population but insufficient facilities

### 🚨 Service Gap Identified
- **Gangdong District**: Seoul's only service gap
  - Senior Population: 96,555 (5th highest)
  - Facilities per 1,000 Seniors: 3.09 (barely exceeds threshold of 3.08)
  - Below average across all facility types

---

## 🔄 Future Improvements
1. **Machine Learning Integration**: District grouping through K-Means clustering
2. **Optimal Location Recommendation**: Priority analysis for deficient facility types
3. **Dashboard Automation**: Interactive web dashboard development using Streamlit
4. **Time Series Analysis**: Prediction of annual senior population growth trends

---

## 📚 References
- [Seoul Open Data Plaza](https://data.seoul.go.kr/)
- [Plotly Official Documentation](https://plotly.com/python/)
- [pandas Official Documentation](https://pandas.pydata.org/)

---

## 📄 License
This project is licensed under the MIT License.

---

**Last Updated**: January 2026  
**Team**: SeSAC Data Analysis Course
