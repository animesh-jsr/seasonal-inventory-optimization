# 🛍️ Seasonal Inventory Optimization for Fast Fashion using the Single Period System

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellow?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-blue?logo=numpy)
![SciPy](https://img.shields.io/badge/SciPy-Statistics-green?logo=scipy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)

---

## 📌 Project Overview

Fast fashion retailers face a major challenge in deciding how much inventory to order before a selling season begins. Since fashion products have a short life cycle and cannot be replenished during the season, ordering too many units results in excess inventory and markdown losses, while ordering too few leads to stockouts and lost sales.

This project implements the  **single-period inventory optimization model**, to determine the optimal order quantity for seasonal apparel products under uncertain demand.

---

## 🎯 Project Objective

Develop a mathematical inventory optimization model that:

- Determines the optimal order quantity for each seasonal product.
- Balances overstock and stockout risks.
- Maximizes expected profit under uncertain demand.
- Supports data-driven inventory planning for fast fashion retailers.

---

## 🏢 Business Scenario

A fast fashion retailer launches a seasonal apparel collection consisting of **20 different SKUs**.

For each product, the retailer knows:

- Purchase Cost
- Retail Price
- Salvage Value
- Expected Demand
- Demand Variability

Since replenishment is not possible after the season starts, the company must determine the optimal inventory level before demand is realized.

---

## 📂 Dataset

The dataset contains **20 seasonal apparel products**.

### Features

| Feature | Description |
|----------|-------------|
| SKU_ID | Product Identifier |
| Item_Description | Product Name |
| Purchase_Cost_c | Procurement Cost |
| Retail_Price_r | Selling Price |
| Salvage_Value_v | End-of-season Liquidation Value |
| Mean_Demand_mu | Expected Seasonal Demand |
| Std_Dev_sigma | Demand Standard Deviation |

---


## 📐 Mathematical Model

The project follows the classical **Single period system** to determine the optimal order quantity for each seasonal product under uncertain demand.

| Metric | Formula | Description |
|--------|---------|-------------|
| **Overage Cost (Co)** | **Co = Purchase Cost − Salvage Value** | Cost incurred for each unsold unit at the end of the season. |
| **Underage Cost (Cu)** | **Cu = Retail Price − Purchase Cost** | Profit lost when customer demand exceeds available inventory. |
| **Critical Ratio (CR)** | **CR = Cu / (Cu + Co)** | Represents the probability of meeting customer demand while balancing overstock and stockout costs. |
| **Z-Value** | **Z = NORM.S.INV(CR)** | Standard normal value corresponding to the calculated critical ratio. |
| **Optimal Order Quantity (Q\*)** | **Q\* = μ + Z × σ** | Determines the inventory level that maximizes expected profit. |

### Where

| Symbol | Meaning |
|---------|---------|
| **μ (Mu)** | Mean (Expected) Demand |
| **σ (Sigma)** | Standard Deviation of Demand |
| **c** | Purchase Cost per Unit |
| **r** | Retail Selling Price |
| **v** | Salvage Value per Unit |
| **Co** | Overage Cost |
| **Cu** | Underage Cost |
| **CR** | Critical Ratio |
| **Z** | Standard Normal Score |
| **Q\*** | Optimal Order Quantity |

---

### Model Assumptions

- Demand follows a **Normal Distribution**.
- Inventory is ordered **once** before the selling season.
- No replenishment is allowed during the season.
- Unsold inventory is liquidated at the salvage value.
- The objective is to maximize expected profit while balancing the risks of overstocking and stockouts.

# ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- SciPy
- Matplotlib
- Jupyter Notebook

---

# 🚀 Project Workflow

```
Demand Dataset
        │
        ▼
Data Preprocessing
        │
        ▼
Calculate Overage Cost
        │
        ▼
Calculate Underage Cost
        │
        ▼
Compute Critical Ratio
        │
        ▼
Calculate Z-Value
        │
        ▼
Determine Optimal Order Quantity
        │
        ▼
Business Analysis
```

---

# 📊 Analysis Performed

The project calculates:

- ✅ Overage Cost
- ✅ Underage Cost
- ✅ Critical Ratio
- ✅ Z-Score
- ✅ Optimal Order Quantity
- ✅ Inventory Investment
- ✅ Expected Revenue
- ✅ Expected Profit
- ✅ Service Level

---

# 📈 Key Results

The model successfully determined the optimal inventory level for all **20 seasonal products**.

Major findings include:

- Products with higher demand uncertainty require larger inventory buffers.
- High-profit products justify higher service levels.
- Premium products with lower demand require conservative inventory planning.
- The Newsvendor Model effectively balances overstock and stockout costs.

---

# 💼 Business Impact

The proposed model enables retailers to:

- Reduce excess seasonal inventory.
- Minimize stockout losses.
- Improve inventory investment decisions.
- Increase expected profitability.
- Support strategic inventory planning under uncertain demand.

---

# 📁 Repository Structure

```
seasonal-inventory-optimization/

│── Seasonal_Inventory_Optimization.ipynb
│── seasonal_inventory.csv
│── Optimal_Order_Results.csv
│── README.md
```

---

# ▶️ How to Run

Clone the repository:

```bash
git clone https://github.com/animesh-jsr/seasonal-inventory-optimization.git
```

Install the required libraries:

```bash
pip install pandas numpy scipy matplotlib
```

Open:

```
Seasonal_Inventory_Optimization.ipynb
```

Run all cells to reproduce the complete analysis.

---

# 🔮 Future Enhancements

- Monte Carlo Demand Simulation
- Multi-Product Inventory Optimization
- Budget-Constrained Optimization using IBM CPLEX
- Multi-Period Inventory Planning
- Warehouse Capacity Constraints
- Supplier Capacity Optimization

---

# 👨‍💻 Author

**Animesh Kumar**

B.Tech, Production and Industrial Engineering  
National Institute of Technology Jamshedpur

**GitHub**

https://github.com/animesh-jsr

**LinkedIn**

https://www.linkedin.com/in/animeshnit

---

