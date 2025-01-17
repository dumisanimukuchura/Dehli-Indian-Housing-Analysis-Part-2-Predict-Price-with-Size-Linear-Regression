# Python for Data Analysis Project 1: Basic EDA

## Project Overview
This project focuses on learning and applying basic data analysis and exploratory data analysis (EDA) techniques using Python. The dataset analyzed contains information about housing rentals in Delhi, India. The project demonstrates data wrangling, data cleaning, and visualizations to answer business-related questions and uncover insights.

## Objectives
- Understand and clean a dataset for analysis.
- Perform exploratory data analysis (EDA) to identify trends and patterns.
- Visualize the data to effectively communicate findings.

---

## Dataset Description
The dataset contains information about housing rentals in Delhi. Below are the columns:

| Column               | Description                                               |
|----------------------|-----------------------------------------------------------|
| `house_type`         | Type of house (e.g., apartment, villa, duplex).           |
| `house_size`         | Size of the house in square feet.                         |
| `location`           | Specific area or neighborhood of the property.            |
| `city`               | City where the property is situated (Delhi).              |
| `latitude`           | Geographic latitude coordinates of the property.          |
| `longitude`          | Geographic longitude coordinates of the property.         |
| `price`              | Rental price of the house in INR.                         |
| `currency`           | Currency in which the price is denoted (e.g., INR).       |
| `numBathrooms`       | Total number of bathrooms in the house.                   |
| `numBalconies`       | Total number of balconies in the house.                   |
| `isNegotiable`       | Indicates whether the price is negotiable (Yes/No).       |
| `priceSqFt`          | Price of the house per square foot.                       |
| `verificationDate`   | Date when the rental information was verified.            |
| `description`        | Additional description or details about the property.     |
| `securityDeposit`    | Amount of security deposit required for renting.          |
| `Status`             | Indicates the furnishing status of the property.          |

---

## Key Data Wrangling Steps
1. **Dropped Duplicates**: Removed duplicate rows to ensure data integrity.
2. **Converted `house_size`**: Removed the \"sq ft\" suffix and converted the column to float.
3. **Price Conversion**:
   - Converted `price` to USD using the exchange rate (1 USD = 85.76 INR).
   - Added a new column `price_approx_usd`.
4. **Calculated `priceSqFt`**:
   - Filled missing values in `priceSqFt` by dividing `price_approx_usd` by `house_size`.
5. **Handled Missing Values**:
   - Replaced `NaN` in `isNegotiable` with \"Not Negotiable\".
   - Dropped rows with remaining `NaN` values.
6. **Standardized Data Types**: Ensured proper data types for numerical and categorical columns.

---

## Key Questions Answered

### **General Analysis**
1. What is the distribution of house types (`house_type`)?
2. Which locations (`location`) have the highest number of rental listings?
3. What is the average price (`price`) for different house types?

### **Price Analysis**
4. How does the size of the house (`house_size`) affect rental prices?
5. Does furnishing status (`Status`) significantly influence rental prices?
6. Is there a noticeable difference in rental prices for negotiable vs. non-negotiable listings?

### **Geospatial Analysis**
7. How are rental prices distributed across latitude and longitude?
8. Are certain areas (based on `latitude` and `longitude`) associated with higher prices?

### **Furnishing and Amenities**
9. Do furnished houses have more bathrooms or balconies than unfurnished ones?
10. What percentage of listings have balconies?

### **Temporal Analysis**
11. How does the `verificationDate` influence rental prices?
12. Are recent listings priced differently from older ones?

---

## Visualizations
The project includes various visualizations to explore and present the data:
- **Bar Plots**: Used to analyze categorical variables like `house_type` and `location`.
- **Scatter Plots**: Explored relationships between numerical variables (e.g., `house_size` vs. `price`).
- **Maps**:
  - Visualized the geographic distribution of properties using `scatter_mapbox`.
  - Highlighted clustering patterns of house types and prices across locations.

---

## Tools and Libraries Used
- **Python**: Primary programming language for analysis.
- **Pandas**: Data manipulation and analysis.
- **NumPy**: Numerical operations.
- **Matplotlib** and **Seaborn**: Data visualization.
- **Plotly**: Interactive maps and advanced visualizations.

---

## How to Run the Project
1. **Set Up the Environment**:
   - Install required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`.
   - Ensure the dataset is placed in the appropriate `data` directory.
2. **Run the Jupyter Notebook**:
   - Open the notebook file in Jupyter or any Python IDE.
   - Execute the cells sequentially.
3. **Explore the Results**:
   - Visualizations and insights are displayed inline in the notebook.

---

## Folder Structure
Dehli-Indian-Housing-EDA/ 
├── data/ 
│ └── Indian_housing_Delhi_data.csv # Dataset file 
├── notebook/ 
│ └── Dehli_Indian_Housing_EDA.ipynb # Jupyter Notebook for analysis 
├── README.md # Project documentation

---

## Project Outcome
- Cleaned and prepared the dataset for analysis.
- Answered key business questions using EDA techniques.
- Visualized patterns and trends to derive actionable insights.

---

## Future Work
- Incorporate advanced machine learning models to predict rental prices.
- Integrate additional datasets for comparative analysis across cities.
- Build an interactive dashboard to present findings dynamically.
"""