# 🚗 EV Energy Consumption Prediction using Machine Learning

## 📌 Project Overview

This project demonstrates how Machine Learning can be used as a **surrogate model** to approximate physics-based electric vehicle (EV) energy consumption calculations.

Instead of repeatedly solving vehicle dynamics equations, a trained ML model can quickly predict energy consumption (Wh/km), making it suitable for real-time applications such as:

- EV range estimation
- Energy optimization
- Simulation acceleration
- Digital twin systems

---

## 🎯 Objective

To predict EV energy consumption (Wh/km) using:

- Vehicle Mass (kg)
- Speed (km/h)
- Acceleration (m/s²)
- Road Gradient (degrees)

The dataset is generated using fundamental vehicle dynamics equations.

---

## 🔬 Physics Background

Total force required to move a vehicle:

F_total = F_rolling + F_aero + F_gradient + F_acceleration

Where:

### 1️⃣ Rolling Resistance
F_rolling = Cr × m × g

### 2️⃣ Aerodynamic Drag
F_aero = 0.5 × ρ × A × Cd × v²

### 3️⃣ Gradient Force
F_gradient = m × g × sin(θ)

### 4️⃣ Acceleration Force
F_acc = m × a

Power required:
P = F_total × v

Energy consumption (Wh/km) is derived from power and vehicle speed.

---

## 📊 Dataset Generation

- Physics-based synthetic data
- Random driving conditions simulated
- Noise added to mimic real-world uncertainty

Features:
- Mass (kg)
- Speed (km/h)
- Acceleration (m/s²)
- Gradient (degrees)

Target:
- Energy Consumption (Wh/km)

---

## 🤖 Machine Learning Models Used

### 1️⃣ Linear Regression
- Baseline model
- Assumes linear relationships

### 2️⃣ Random Forest Regressor
- Captures nonlinear behavior
- Handles aerodynamic drag (v² effect) effectively

---

## 📈 Model Evaluation Metrics

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score
- Actual vs Predicted Visualization
- Feature Importance Analysis

---

## 🔥 Key Insights

- Aerodynamic drag increases with velocity squared (v²)
- Power demand increases rapidly at high speeds
- Acceleration and uphill driving significantly increase energy consumption
- Random Forest outperforms Linear Regression due to nonlinear relationships

---

## 🛠 Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## 🚀 How to Run

1. Clone this repository:

   git clone https://github.com/your-username/ev-energy-ml.git

2. Install dependencies:

   pip install numpy pandas matplotlib scikit-learn

3. Run the Python script or open the Jupyter Notebook.

---

## 📌 Future Improvements

- Add motor efficiency modeling
- Include regenerative braking effects
- Use real-world EV datasets
- Hyperparameter tuning
- Cross-validation
- Add Gradient Boosting model

---

## ⭐ Project Summary

This project combines:

- Vehicle dynamics fundamentals
- Physics-based modeling
- Machine Learning regression
- Engineering interpretation

It demonstrates how ML can effectively approximate physics-driven energy models in electric vehicles.
