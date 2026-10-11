# SpaceX Falcon 9 First Stage Landing Prediction

**Applied Data Science Capstone: IBM Data Science Professional Certificate**

This project predicts whether the first stage of a SpaceX Falcon 9 rocket will land successfully. SpaceX advertises Falcon 9 launches at a much lower price than its competitors, largely because the first stage can be reused. If we can predict the landing outcome, we can estimate the cost of a launch, which is useful for any company that wants to bid against SpaceX.

The project follows the full data science workflow: data collection, wrangling, exploratory analysis, interactive visualization, and machine learning.

> **Course:** [Applied Data Science Capstone](https://www.coursera.org/learn/applied-data-science-capstone) (course 10 of the [IBM Data Science Professional Certificate](https://www.coursera.org/professional-certificates/ibm-data-science))

---

## Project Workflow

| Step | Notebook / File | What it does |
|------|-----------------|--------------|
| 1 | [Data Collection API](./Space%20X%20Falcon%209%20First%20Stage%20Landing%20Prediction%20Data%20Collection%20API.ipynb) | Collects launch data from the SpaceX API |
| 2 | [Data Collection with Web Scraping](./Space%20X%20Falcon%209%20First%20Stage%20Landing%20Prediction%20Data%20Collection%20with%20Web%20Scraping.ipynb) | Scrapes launch records from a web page |
| 3 | [Data Wrangling](./Space%20X%20Falcon%209%20First%20Stage%20Landing%20Prediction%20Data%20Wrangling.ipynb) | Cleans the data and creates the landing outcome label |
| 4 | [EDA with SQL](./Space%20X%20Falcon%209%20First%20Stage%20Landing%20Prediction%20the%20EDA%20with%20SQL.ipynb) | Explores the data with SQL queries |
| 5 | [EDA with Visualization](./Space%20X%20Falcon%209%20First%20Stage%20Landing%20Prediction%20EDA%20with%20Visualization.ipynb) | Explores relationships between features with charts |
| 6 | [Interactive Visual Analytics with Folium](./Space%20X%20Falcon%209%20First%20Stage%20Landing%20Prediction%20Interactive%20Visual%20Analytics%20with%20Folium.ipynb) | Maps the launch sites and their surroundings |
| 7 | [Interactive Dashboard with Plotly Dash](./Space%20X%20Falcon%209%20First%20Stage%20Landing%20Prediction%20Interactive%20Dashboard%20with%20Plotly%20Dash.py) | Dashboard to explore launch success by site and payload |
| 8 | [Machine Learning Prediction](./Space%20X%20Falcon%209%20First%20Stage%20Landing%20Prediction%20Machine%20Learning%20Prediction.ipynb) | Trains and compares classification models |
| 9 | [Capstone Presentation](./ms82etojxrrm92wzqti-SpaceX%20Falcon%209%20Landing%20Prediction%20Capstone.pptx) | Final presentation of the results |

**Data file:** [`spacex_launch_dash.csv`](./Space%20X%20Falcon%209%20First%20Stage%20Landing%20Prediction%20spacex_launch_dash.csv) is the dataset used by the Plotly Dash dashboard.

## Tools & Libraries

**Language:** Python, SQL
**Data handling:** Pandas, NumPy
**Data collection:** SpaceX REST API (`requests`), web scraping (BeautifulSoup)
**Visualization:** Matplotlib, Seaborn, Folium, Plotly, Dash
**Machine learning:** Scikit-learn
**Environment:** Jupyter Notebook

## Methodology

1. **Data collection:** launch data is gathered from the SpaceX API and a second source via web scraping, then combined into one dataset.
2. **Data wrangling:** missing values are handled, and each launch is labeled as a successful or failed landing (`Class` = 1 or 0).
3. **Exploratory analysis with SQL:** queries on launch sites, payload mass, booster versions, and mission outcomes.
4. **Exploratory analysis with visualization:** charts comparing flight number, payload, launch site, orbit, and booster version against landing success.
5. **Interactive analytics:** Folium maps with markers, success/failure clusters, and distances from launch sites to nearby features, plus a Plotly Dash dashboard with a launch site selector and a payload range slider.
6. **Predictive modeling:** features are standardized and split into training and test sets. Classification models (logistic regression, SVM, decision tree, and k-nearest neighbors) are tuned with grid search and compared on test accuracy.


<!-- Optional: add screenshots
![Confusion matrix](images/confusion_matrix.png)
![Dashboard](images/dashboard.png) -->

## Getting Started

```bash
# Clone the repository
git clone https://github.com/LahcenAmroune/Applied-Data-Science-Capstone.git
cd <Applied-Data-Science-Capstone>

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn folium plotly dash requests beautifulsoup4 jupyterlab

# Run the notebooks in order
jupyter lab
```

### Run the dashboard

```bash
python "Space X Falcon 9 First Stage Landing Prediction Interactive Dashboard with Plotly Dash.py"
```

Then open the local address shown in the terminal (usually `http://127.0.0.1:8050`). Keep `spacex_launch_dash.csv` in the path the script expects.

## Repository Structure

```
.
├── Data Collection API.ipynb
├── Data Collection with Web Scraping.ipynb
├── Data Wrangling.ipynb
├── the EDA with SQL.ipynb
├── EDA with Visualization.ipynb
├── Interactive Visual Analytics with Folium.ipynb
├── Interactive Dashboard with Plotly Dash.py
├── Machine Learning Prediction.ipynb
├── spacex_launch_dash.csv
├── SpaceX Falcon 9 Landing Prediction Capstone.pptx
└── README.md
```

*(Each file name begins with "Space X Falcon 9 First Stage Landing Prediction", shortened here for readability.)*

## What I Learned

- How to build a data science project end to end, from raw data to a predictive model
- Collecting data from a REST API and by web scraping, and combining the sources
- Using SQL for exploratory analysis, and charts and maps to find patterns
- Building an interactive dashboard with Plotly Dash
- Comparing classification models and tuning them with cross-validation

## Acknowledgements

Course material and project structure by [IBM](https://www.coursera.org/partners/ibm-skills-network) via [Coursera](https://www.coursera.org). Launch data comes from the SpaceX API and public web sources. This repository contains my own solutions for learning purposes.

## Contact

**Lahcen AMROUNE**
[LinkedIn](www.linkedin.com/in/lahcen-mokhtar-amroune) · [Email](mailto:amrounelahce91@gmail.com)
