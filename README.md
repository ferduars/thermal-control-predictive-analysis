# Predictive Modeling for On/Off Thermal Control

This project demonstrates the application of **Logistic Regression** to predict the operational state of a transistor's On/Off controller. By analyzing temperature trends and calculating derivatives, the model identifies whether the heating element is active based on thermal behavior.

## 🌡️ The Problem
In control systems, the state of an actuator (On/Off) is typically a known input. This project flips the perspective: **Can we predict the controller's decision solely by looking at the temperature data?**

## 🛠️ Methodology & Tech Stack
* [cite_start]**Data Collection:** Real-time data acquisition using the **TCLab (Temperature Control Lab)** and Arduino[cite: 61].
* **Feature Engineering:** Calculated the **1st and 2nd derivatives** of temperature ($dT/dt$) to provide the model with "velocity" and "acceleration" data of the heat transfer.
* **Preprocessing:** Utilized `MinMaxScaler` to normalize features for better convergence of the regression model.
* [cite_start]**Modeling:** Implemented a **Logistic Regression** classifier using `Scikit-Learn`[cite: 59].

## 📊 Key Results
The model successfully differentiates between active heating and passive cooling phases. 
* **Target Variable:** Transistor State ($Q_1 \in \{0, 100\}$).
* **Input Features:** Temperature ($T_1$), Rate of Temperature Change ($dT_1$), and Thermal Acceleration ($d^2T_1$).

## 🚀 Installation & Usage
1. Clone the repository.
2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
