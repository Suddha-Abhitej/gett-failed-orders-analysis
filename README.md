# 🚖 Gett Failed Orders Analysis

This project analyzes failed ride orders from Gett (formerly GetTaxi), a corporate ground transportation platform. The data was used as a take-home assignment for data science candidates at Gett.

## 📁 Dataset Overview

We use two CSV files:

1. **`data_orders.csv`**  
   Contains order-level information:
   - `order_datetime`, `origin_latitude`, `origin_longitude`
   - `m_order_eta` (estimated arrival)
   - `order_status_key` (4 = cancelled by client, 9 = rejected by system)
   - `is_driver_assigned_key`
   - `cancellation_time_in_seconds`

2. **`data_offers.csv`**  
   Contains mappings of `order_gk` to individual `offer_id`s (driver offers).

---

## 🎯 Objectives

### Core Tasks
- 📊 Distribution of orders by failure reason:
  - Cancelled before driver assignment
  - Cancelled after driver assignment
  - Rejected by system
- ⏱️ Analyze time-based failure patterns (hourly)
- 📉 Plot average cancellation time by hour and assignment status
- 🕓 Visualize average ETA trends over time
- 🗺️ **Bonus**: Create an H3 hex map with `folium` showing high-failure geospatial clusters

---

## 🔍 Key Insights

- Most cancellations occurred **before a driver was assigned**
- **Late evenings and early mornings** saw the highest failure rates
- Users waited **longer to cancel** when a driver was already assigned
- Certain areas had disproportionately higher failure density (visualized using H3 hexes)

---

## 📚 Tech Stack

- **Python**, **Pandas**, **NumPy**, **Seaborn**, **Matplotlib**
- **H3** for hex spatial indexing
- **Folium** for mapping failures by location
- **Google Colab** for notebook development

---

## 📁 Project Structure

gett-failed-orders-analysis/
│
├── data/ # Input CSV files
├── notebooks/ # Step-by-step analysis
├── src/ # Helper scripts (plotting, cleaning, etc.)
├── visuals/ # Saved charts and maps
├── README.md # Project documentation
└── requirements.txt # Python dependencies

🧠 Author
Suddha Abhitej
Data Science Enthusiast | Problem-Solver | Analytics Explorer

