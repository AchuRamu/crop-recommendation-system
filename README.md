# Crop Recommendation System: Precision Agriculture through Unsupervised Learning

## Project Overview

This project develops an intelligent crop recommendation system using unsupervised machine learning techniques to optimize agricultural decision-making. By analyzing soil conditions, climate data, and environmental factors, the system provides data-driven crop recommendations to enhance agricultural productivity and sustainability.

## Business Problem

Modern agriculture faces critical challenges in crop selection optimization:
- **Farmers**: Need data-driven guidance for crop selection based on soil and climate conditions
- **Agricultural Consultants**: Require analytical tools for evidence-based recommendations
- **Food Security**: Optimizing crop yield through scientific approach to agriculture
- **Sustainable Farming**: Reducing resource waste through appropriate crop-soil matching

## Dataset Description

**Dataset:** Agricultural Crop Recommendation Dataset  
**Size:** 2,200 samples across 22 different crops  
**Source:** Comprehensive agricultural research data  

### Environmental Features:
- **N, P, K**: Nitrogen, Phosphorous, and Potassium content ratios in soil
- **Temperature**: Environmental temperature in Celsius
- **Humidity**: Relative humidity percentage
- **pH**: Soil acidity/alkalinity levels
- **Rainfall**: Annual precipitation in millimeters

### Crop Categories (22 types):
Rice, Maize, Jute, Cotton, Coconut, Papaya, Orange, Apple, Muskmelon, Watermelon, Grapes, Mango, Banana, Pomegranate, Lentil, Blackgram, Mungbean, Mothbeans, Pigeonpeas, Kidneybeans, Chickpea, Coffee

## Methodology

### Data Analysis & Preprocessing
- **Exploratory Data Analysis**: Comprehensive analysis of 2,200 crop samples
- **Feature Engineering**: Soil composition and climate factor analysis
- **Correlation Analysis**: NPK relationships and climate-rainfall patterns
- **Data Standardization**: Z-score normalization for clustering algorithms
- **Outlier Detection**: Statistical identification and handling of extreme values

### Unsupervised Learning Models

#### 1. K-Means Clustering
- **Implementation**: Elbow method for optimal cluster determination
- **Evaluation**: Silhouette Score = 0.227
- **Findings**: Limited cluster separation, suggesting complex crop-environment relationships

#### 2. Hierarchical Clustering
- **Linkage Methods**: Average, Complete, Ward linkage comparison
- **Best Performance**: Ward linkage method
- **Evaluation**: Silhouette Score = 0.394 (highest performance)
- **Visualization**: Dendrogram analysis for cluster structure

#### 3. UMAP (Uniform Manifold Approximation)
- **Hyperparameter Tuning**: Neighbors and distance optimization
- **Dimensionality Reduction**: 2D visualization for pattern identification
- **Result**: Limited cluster formation despite parameter adjustment

### Key Agricultural Insights

#### Soil Composition Analysis
- **High NPK Requirements**: Grapes, Apple (K>200), Cotton, Coffee (N>100)
- **Low NPK Crops**: Lentil, Orange, Kidneybeans (efficient nutrient utilization)
- **NPK Correlation**: Strong positive correlation between Potassium and Phosphorous

#### Climate Preferences
- **High Temperature Crops**: Papaya (33.7°C), Mango (31.2°C)
- **High Humidity Requirements**: Coconut (94.8%), Papaya (92.4%)
- **Rainfall Patterns**: Rice (236mm), Coconut (175mm) vs. Lentil (45mm)

## Tools and Technologies

- **Python**: Core programming and analysis
- **Pandas & NumPy**: Data manipulation and numerical computing
- **Scikit-learn**: Machine learning algorithms and evaluation
- **Matplotlib & Seaborn**: Statistical visualizations
- **Plotly**: Interactive agricultural data visualizations
- **UMAP**: Advanced dimensionality reduction
- **SciPy**: Statistical analysis and correlation testing

## Model Performance Comparison

| Model | Method | Silhouette Score | Recommendation |
|-------|--------|------------------|----------------|
| Hierarchical | Ward Linkage | 0.394 | ✅ **Best Performance** |
| K-Means | Standard | 0.227 | Moderate |
| Hierarchical | Complete | 0.186 | Limited |
| Hierarchical | Average | 0.175 | Limited |

**Recommended Model**: Hierarchical Clustering with Ward linkage method demonstrates superior cluster quality and agricultural pattern recognition.

## Agricultural Applications

### For Farmers
- **Soil-Based Recommendations**: Data-driven crop selection based on soil composition
- **Climate Matching**: Optimal crop choices for local environmental conditions
- **Yield Optimization**: Scientific approach to maximize agricultural productivity

### For Agricultural Consultants
- **Evidence-Based Advice**: Quantitative support for crop recommendations
- **Risk Assessment**: Understanding crop suitability for specific conditions
- **Resource Planning**: Efficient allocation of fertilizers and water resources

### For Policy Makers
- **Food Security Planning**: Regional crop optimization strategies
- **Sustainable Agriculture**: Environmentally conscious farming recommendations
- **Economic Impact**: Crop selection for maximum economic return

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/AchuRamu/crop-recommendation-system.git
   cd crop-recommendation-system
   ```

2. Install required dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn plotly umap-learn scipy
   ```

3. Open the Jupyter notebook:
   ```bash
   jupyter notebook crop-recommendation-analysis.ipynb
   ```

4. Run all cells to reproduce the analysis

### Dataset Requirements
The analysis uses `Crop_recommendation.csv` containing agricultural data with soil and climate measurements.

*Note: Original analysis conducted in Google Colab. Paths updated for local execution.*

## Project Structure

```
crop-recommendation-system/
│
├── crop-recommendation-analysis.ipynb    # Main analysis notebook
├── README.md                            # Project documentation
├── data/                                # Agricultural datasets
├── models/                              # Clustering model artifacts
└── visualizations/                      # Agricultural analysis charts
```

## Key Findings

### Scientific Insights
- **Ward Hierarchical Clustering** provides optimal crop grouping with 39.4% silhouette score
- **NPK Correlation**: Strong relationship between Potassium and Phosphorous requirements
- **Climate Specialization**: Clear patterns in temperature and humidity preferences across crops
- **Resource Efficiency**: Identification of low-input, high-yield crop categories

### Agricultural Recommendations
- **Precision Agriculture**: Soil testing enables targeted crop selection
- **Resource Conservation**: Matching crops to natural conditions reduces input requirements
- **Yield Maximization**: Data-driven approach improves agricultural outcomes
- **Sustainable Practices**: Environmentally appropriate crop selection

## Future Enhancements

- **Real-time Integration**: IoT sensor data for dynamic recommendations
- **Economic Modeling**: Market price integration for profit optimization
- **Regional Adaptation**: Geographic-specific recommendation systems
- **Climate Change**: Adaptation strategies for changing environmental conditions

## Contact

**Archana Ramachandran**  
Data Scientist | Software Engineer  
📧 aramach82@gmail.com  
🔗 LinkedIn: [linkedin.com/in/archana-ramachandran](https://www.linkedin.com/in/archana-ramachandran)

---

*This project demonstrates expertise in unsupervised learning, agricultural data science, clustering analysis, and precision agriculture applications using advanced machine learning techniques.*
