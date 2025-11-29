# 🌊 Water Quality Analysis Using Satellite Images  
*A data-driven exploration of water quality prediction using multispectral satellite imagery and machine learning.*

---

## 📌 **Project Overview**

This project analyzes water quality indicators using **satellite-derived features** and classical machine learning.  
It demonstrates how reflectance bands and simple spectral indices can be used to model water quality trends, evaluate feature relationships, and build reproducible predictive pipelines.

The entire analysis is implemented in a single, clean Jupyter notebook:
```
notebooks/final_water_quality_analysis_april17.ipynb
```

The workflow covers:

- Data loading & cleaning  
- Feature engineering from spectral bands  
- Exploratory analysis  
- Predictive modeling  
- Result visualization  
- Recommendations for future extensions  

---

## 🛰️ **Motivation**

Remote sensing provides an efficient way to monitor large water bodies without the need for expensive field sampling.  
By using satellite images, we can estimate parameters such as:

- Turbidity  
- Chlorophyll-related activity  
- Suspended solids  
- Water clarity  

This project demonstrates a **scalable, low-cost** method to approximate these indicators from readily available multispectral data.

---

## 🗂 **Repository Structure**
```
Water-Quality-Analysis-using-Satellite-Images/
├── notebooks/
│ └── final_water_quality_analysis_april17.ipynb # Main analysis
├── data/ # Raw/processed data (gitignored)
├── results/ # Exported plots & model outputs
├── requirements.txt # Python dependencies
└── README.md
```
---

## 🧪 **Workflow Summary**

### **1. Data Import & Cleaning**
The notebook loads a tabular dataset containing:

- Reflectance band values (e.g., Blue, Green, Red, NIR)  
- Derived indices  
- Ground-truth water quality variables  

Cleaning steps include:

- Handling invalid values  
- Removing noise/outliers  
- Normalizing numeric variables  
- Basic exploratory checks  

---

### **2. Feature Engineering**

The project derives meaningful predictors such as:

- Band ratios  
- Reflectance differences  
- Simple spectral indices  
- Normalized variables  

Example engineered features:

- `NIR / Red`  
- `Green / Blue`  
- `log10(reflectance + ε)`  

These variables often correlate well with turbidity, particulate concentration, and phytoplankton activity.

---

### **3. Exploratory Data Analysis**

The notebook visualizes:

- Distributions of spectral features  
- Correlation heatmaps  
- Scatterplots between reflectance bands and water quality metrics  
- Basic spatial/temporal behavior (if applicable)

This step helps identify relationships and guides model selection.

---

### **4. Modeling**

The notebook tests classical ML regressors/classifiers such as:

- Linear Regression  
- Decision Trees  
- Random Forest (optional)  
- Train/validation/test splits  

Each model is evaluated using:

- RMSE  
- MAE  
- R² score  
- Visual predicted vs actual plots  

The goal is to check whether spectral features can consistently predict water quality parameters.

---

### **5. Visualization & Interpretation**

Outputs include:

- Prediction curves  
- Residual plots  
- Top feature contributions  
- Example maps (if geolocation available)  

Visuals are saved into the `results/` directory for easy export.

---

## 🧰 **Installation & Setup**

### **1. Clone the repository**
```bash
git clone https://github.com/paritosh100/Water-Quality-Analysis-using-Satellite-Images.git
cd Water-Quality-Analysis-using-Satellite-Images
```
2. Create & activate a virtual environment
```bash
Copy code
python -m venv .venv
source .venv/bin/activate     # Windows: .venv\Scripts\activate
```
3. Install dependencies
``bash
Copy code
pip install -r requirements.txt
```
4. Launch Jupyter
```bash
Copy code
jupyter notebook
Open the notebook:
Copy code
notebooks/final_water_quality_analysis_april17.ipynb
```
📦 Dependencies

Listed in requirements.txt, including:
```
numpy

pandas

matplotlib

seaborn

scikit-learn

jupyter

(Geospatial libraries such as rasterio, folium, or geopandas may be added if you expand the analysis.)
```
📊 Results Summary
- The notebook generates:

- Cleaned dataset

- Feature correlations

- Regression model performance metrics

- Visualization of predicted vs actual values

- Insights into which spectral features best predict water parameters

- These results demonstrate the feasibility of using multispectral features to approximate water quality indicators.

🚧 Limitations
- Dataset size may be limited

- Only simple spectral features evaluated

- No atmospheric correction pipeline included

- Synthetic/curated data may not perfectly match real-world conditions

🔮 Future Improvements
- Potential enhancements:

- Integrate Landsat-8/Sentinel-2 raw imagery

- Add more complex spectral indices

- Use advanced ML models (XGBoost, LightGBM)

- Build SHAP-based feature explanations

- Create an interactive Streamlit dashboard

- Include spatial mapping (lat/lon) with folium

✨ Author
Paritosh Kiran Gandre
M.S. in Data Science, Kent State University

- Portfolio: https://paritosh-gandre.vercel.app

- GitHub: https://github.com/paritosh100

- LinkedIn: https://linkedin.com/in/paritosh-gandre

Gandre, P. (2025). Water Quality Analysis using Satellite Images.

GitHub Repository: https://github.com/paritosh100/Water-Quality-Analysis-using-Satellite-Images
