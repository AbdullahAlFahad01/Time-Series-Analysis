# 📊 Time Series Analysis (Beginner to Intermediate Guide)

---

## 🔹 Part 1: Introduction to Time Series

Time Series হলো এমন একটি ডাটা অ্যানালাইসিস পদ্ধতি যেখানে সময়ের ক্রম অনুযায়ী সাজানো ডাটা ব্যবহার করে ভবিষ্যতের একটি মান **Forecast / Prediction** করা হয়।

### 📌 Example
ধরুন একটি দোকানের বিক্রি:
- Day 1 → 20 টাকা  
- Day 2 → 30 টাকা  
- Day 3 → 50 টাকা  

এখন আমরা predict করতে চাই Day 4 এর বিক্রি কত হতে পারে।  
এই প্রক্রিয়াকেই বলা হয় **Time Series Forecasting**।

---

### 📷 Visualization
![Time Series Example](time1.png)

---

## 📍 কোথায় ব্যবহার হয়?
- Business Sales Forecasting  
- Stock Market Analysis  
- Weather Forecasting  
- Demand Prediction  
- Energy Consumption Forecasting  

---

## 🔑 Time Series Components

### 🔹 Trend
দীর্ঘমেয়াদী প্রবণতা (Upward / Downward)

**Example:**
- Company sales বৃদ্ধি পাচ্ছে  
- YouTube subscriber বাড়ছে  
- Business revenue কমছে  

**Use Cases:**
- Business Growth Analysis  
- Revenue Forecasting  
- Market Trend Analysis  

---

### 🔹 Seasonality
নির্দিষ্ট সময় পরপর repeat হওয়া pattern

**Example:**
- গরমে আইসক্রিম বিক্রি বেশি  
- ঈদে কাপড়ের বিক্রি বেশি  
- শীতে গরম কাপড়ের চাহিদা বেশি  

**Use Cases:**
- Retail Sales  
- Tourism  
- Fashion Industry  

---

### 🔹 Cyclical Pattern
দীর্ঘমেয়াদী ওঠানামা (economic/business cycle)

**Example:**
- Boom & Recession  
- Stock market ওঠানামা  
- Industry performance cycles  

**Use Cases:**
- Economic Analysis  
- Stock Market  
- Business Cycle Study  

---

### 🔹 Irregular / Random Variation
হঠাৎ unpredictable পরিবর্তন

**Example:**
- Breaking news → stock jump  
- Natural disaster → business impact  
- Viral trend → demand spike  

**Use Cases:**
- Risk Analysis  
- Market Volatility  
- Crisis Impact  

---

# 🔹 Part 2: Time Series Decomposition

Time Series Decomposition এর মাধ্যমে data কে ৩টি অংশে ভাগ করা হয়:

- **Trend** → Long-term direction  
- **Seasonality** → Repeating pattern  
- **Residual (Noise)** → Random variation  

---

### 📷 Decomposition Visualization
![Decomposition](decom.png)

---

## ⚙️ Decomposition Methods

### 🔹 Classical Decomposition
- Moving Average ব্যবহার করে Trend বের করা হয়  
- Components: Trend + Seasonal + Residual  

#### Model Types:
- **Additive Model** → seasonal constant  
- **Multiplicative Model** → seasonal changes with trend  

⚠️ Limitation:
- Outlier handle করতে পারে না  
- Fixed seasonality ধরে নেয়  

---

### 🔹 STL Decomposition (Modern)
**Full Form:** Seasonal-Trend Decomposition using LOESS  

- LOESS smoothing ব্যবহার করে  
- Only Additive Model  
- Better for real-world noisy data  

✅ Advantages:
- Handles outliers better  
- Flexible seasonality  
- Smooth trend  

---

## 📍 Additive Model Use Cases
- Temperature  
- Electricity Demand  
- Traffic Volume  
- Hospital Visits  
- Agriculture Production  

---

# 🔹 Part 3: Stationarity

Time Series Analysis এর সবচেয়ে গুরুত্বপূর্ণ concept হলো **Stationarity** 📊

### 📌 Definition
যখন নিচেরগুলো time এর সাথে change করে না:
- Mean  
- Variance  
- Autocorrelation  

👉 তখন data **stationary**

---

### ❗ কেন গুরুত্বপূর্ণ?
কারণ বেশিরভাগ forecasting model (যেমন ARIMA)  
👉 **stationary data তে ভালো কাজ করে**

---

### 📷 Stationarity Visualization
![Stationary vs Non-Stationary](stationary.png)

---

## 🔍 Stationarity Check Methods

### ✔️ 1. Graph Method
- Mean/variance change → Non-stationary  

### ✔️ 2. ADF Test
- p-value < 0.05 → Stationary  
- p-value > 0.05 → Non-stationary  

---

## 🔄 Transformation Techniques

যদি data non-stationary হয়:
- Differencing  
- Log Transformation  
- Smoothing  

---

## 🚀 Time Series Workflow

```text
Decomposition 
   ↓
Stationarity Check 
   ↓
Transformation 
   ↓
Modeling
