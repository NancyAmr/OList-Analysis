## 💾 Dataset Source

The analysis is based on the **Brazilian E-Commerce Public Dataset by Olist**, which is publicly available on Kaggle:
👉 [Olist E-Commerce Dataset on Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
# 📊 Olist E-Commerce Data Analysis & Logistics Insights

An end-to-end data analytics project focused on exploring Brazilian e-commerce marketplace dynamics using the **Olist Dataset**. This project uncovers critical operational bottlenecks, catalog structures, and supply chain imbalances that directly impact delivery performance and customer satisfaction.

---

## 🚀 Key Business Insights Uncovered

### 🗺️ 1. Supply vs. Market Coverage Mismatch (The Logistics Crisis)
* **The Finding:** While Olist covers a massive network of **5,955 cities** across all 27 Brazilian states, its merchant supply chain is heavily centralized. 
* **The Core Bottleneck:** **59.7% of all unique sellers are located in a single state (São Paulo - SP)**, with 22.4% concentrated in São Paulo city alone. 
* **The Impact:** Shipping packages from one central cluster across a nationwide network strains operations, leading to a major shipping crisis where **over 44,300+ orders suffer from a 10+ days delivery delay**.

### 📦 2. Product Catalog & Data Quality Red Flags
* **Category Dominance:** The platform’s product variety is heavily driven by **Home Goods & Lifestyle** segments. The Top 5 categories (led by `cama_mesa_banho` - Bed, Table & Bath) represent **over 40%** of the entire marketplace catalog.
* **Data Quality Red Flags:** Identified a physical impossibility in the product specifications where the minimum recorded weight was **0.0 grams**, signaling a clear data-entry error by merchants. Additionally, **610 products** are completely missing descriptions, categories, and photos, which harms conversion rates.
* **Heavy Logistics Strain:** Identified **1,635 unusually heavy products** (top 5% of the catalog reaching up to 40.4 kg) that require expensive, specialized freight shipping, contributing to the delivery delays.

---

## 🧹 Data Cleaning & Preprocessing Highlights

* **Geospatial Aggregation:** Handled **261,831 duplicate coordinates** in the geolocation table. Used aggregation techniques (`groupby().mean()`) to establish one unique center point per zip code prefix, ensuring clean downstream data merging without data explosion.


---

## 🛠️ Tech Stack Used

* **Language:** Python
* **Libraries:** Pandas, NumPy (for data manipulation and cleaning)
* **Visualization:** Plotly Express (for interactive charts and trend analysis)
