# 🔋 Lithium-Ion Battery Remaining Useful Life (RUL) Prediction using LSTM

## 📌 Overview
Lithium-ion batteries are widely used in laptops, smartphones, and electric vehicles due to their **high energy density** and **long cycle life**.  
However, their health degrades over time depending on charge/discharge cycles, current, voltage, temperature, and depth of discharge.  

This project develops a **Long Short-Term Memory (LSTM)** deep learning model to predict **battery capacity degradation** and estimate the **Remaining Useful Life (RUL)** from charging cycle profiles.

---

## 🎯 Objectives
- Predict **capacity fade** and **State of Health (SoH)** of Li-ion batteries.  
- Estimate **Remaining Useful Life (RUL)** for preventive maintenance and safe operation.  
- Benchmark deep learning (LSTM) against conventional approaches.

---

## 🗂️ Dataset
- **Source:** [NASA Ames Prognostics Data Repository](https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/)  
- Contains battery degradation data under various load/temperature conditions.  
- Features: **voltage, current, temperature, capacity vs. cycle index**.  

References:  
1. Choi, Yohwan, et al. *"Machine Learning-Based Lithium-Ion Battery Capacity Estimation Exploiting Multi-Channel Charging Profiles."* IEEE Access 7 (2019): 75143-75152.  
2. Saha, B., & Goebel, K. (2007). *"Battery Data Set."* NASA Ames Prognostics Data Repository.  

---

## 🔧 Methodology
1. **Data Preprocessing**
   - Loaded NASA Ames dataset.  
   - Extracted cycle-wise voltage, current, and temperature signals.  
   - Normalized and structured time-series data for LSTM input.  

2. **Model Architecture (LSTM)**
   - Input: Sequences of voltage, current, temperature readings.  
   - 2 stacked LSTM layers + Dense output layer.  
   - Loss: Mean Squared Error (MSE).  
   - Optimizer: Adam.  

3. **Training**
   - Train/validation split with cross-cycle validation.  
   - Epochs: 100+ (tuned with early stopping).  
   - Batch size: 32.  

---

## 📊 Results
- Achieved ~**4% Mean Absolute Percentage Error (MAPE)** in SoH estimation.  
- LSTM effectively captured **temporal degradation patterns** in battery cycles.  
- Demonstrated reliable forecasting of **battery capacity decline** and **RUL**.  




---

## 🛠️ Tech Stack
- **Languages:** Python  
- **Frameworks:** TensorFlow/Keras  
- **Libraries:** NumPy, Pandas, Matplotlib, Scikit-learn  
- **Environment:** Jupyter Notebook  

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/LSTM-Battery-RUL.git
   cd LSTM-Battery-RUL
