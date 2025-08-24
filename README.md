# STGNN-LogReturn-Prediction

This repository implements a **Spatio-Temporal Graph Neural Network (STGNN)** for predicting stock **log returns**.  
The project combines **graph structure learning** with **time series modelling**, aiming to capture both cross-sectional relations between stocks and temporal dynamics.

---

## 🔍 Project Overview
- **Goal**: Forecast short-term log returns of selected stocks.  
- **Approach**: Use STGNN to jointly model **industry relationships** (graph structure) and **historical log return sequences**.  
- **Application**: Quantitative finance, factor modelling, trading signal generation.  

---

## ⚙️ Methodology
1. **Graph Construction**  
   - Static graph built from industry classification (`Sub-Industry` adjacency).  
   - Each stock is a node, edges represent similarity/industry relations.  

2. **Temporal Module**  
   - LSTM / GRU to model sequential log returns.  
   - Sliding window of historical returns as input.  

3. **STGNN Integration**  
   - Graph Convolution (GCN) layer captures spatial dependencies.  
   - Temporal module captures time dynamics.  
   - Final layer outputs next-day predicted log return.  

---

## 📊 Data
- **Universe**: S&P500 sample of 100 stocks (customisable).  
- **Target**: Standardised 1-day log returns (`log_return_1d`).  
- **Storage**: MySQL / CSV (configurable).  
- **Note**: Due to GitHub file size limits, only sample datasets are included.  
  Full datasets can be downloaded separately (see `data/README.md`).  

---

## 📂 Repository Structure
