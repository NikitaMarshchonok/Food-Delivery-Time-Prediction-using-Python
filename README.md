# Food Delivery Time Prediction (Python)

Accurately predicting delivery time helps food delivery apps keep customer expectations realistic and optimize logistics.  
This project builds an end-to-end **ML regression** pipeline in a Jupyter notebook to predict the **time taken (minutes)** using rider and order features.

<p align="center">
  <img src="pic/1.png" alt="Distance vs Time" width="85%">
</p>

---

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Repository Structure](#repository-structure)
- [Exploratory Analysis](#exploratory-analysis)
- [Modeling](#modeling)
- [How to Run](#how-to-run)
- [Results & Example Inference](#results--example-inference)
- [Next Steps](#next-steps)
- [License](#license)

---

## Project Overview
We predict delivery time using:
- **Distance** between restaurant and destination (computed with the **Haversine** formula from lat/long),
- **Delivery partner Age** and **Ratings**,
- plus categorical context (vehicle / order type) explored in EDA.

The current baseline is a simple **Keras LSTM → Dense** regressor trained on engineered features.

---

## Dataset
- File: `Delivery time/deliverytime.txt` (CSV-like text with headers)
- Key columns:  
  `Delivery_person_Age`, `Delivery_person_Ratings`,  
  `Restaurant_latitude`, `Restaurant_longitude`,  
  `Delivery_location_latitude`, `Delivery_location_longitude`,  
  `Type_of_order`, `Type_of_vehicle`, `Time_taken(min)`
- A new feature **`distance`** is computed from coordinates.

> If you use your own data, keep column names or adapt paths/cell code in the notebook.

---

## Repository Structure
