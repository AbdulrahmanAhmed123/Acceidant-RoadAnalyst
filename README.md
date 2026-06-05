# Acceidant-RoadAnalyst
# 🚗 Road Accident Data Analysis & Root Cause Exploration

مرحباً بك في مشروع **Acceidant-RoadAnalyst**! هنا بنقوم برحلة تحليلية لاستكشاف بيانات حوادث الطرق وفهم الأسباب الرئيسية (**Root Causes**) اللي بتؤدي للحوادث دي، وازاي ظروف الطريق والطقس بتأثر على سلامة الحركة المرورية.

---

## 📌 Overview (نظرة عامة)
الملف ده عبارة عن **Jupyter Notebook (`Root_cause_accident.ipynb`)** شغالين فيه على مرحلة الـ **Data Cleaning & Exploration**. هدفنا الأساسي في هذا الجزء هو تجهيز البيانات وتنظيفها وتصليح الـ **Data Types** عشان تكون جاهزة للـ **Visualization** والـ **Analysis** المتقدم.

البيانات مبنية على عينة ضخمة تحتوي على أكثر من **102,000 سجل** لبيانات حوادث الطرق.

---

## 🛠️ Tech Stack & Libraries Used
استخدمنا في النوت بوك ده أشهر مكتبات الـ **Data Science** في بايثون:
* **Pandas:** عشان الـ Data Manipulation وقراءة الملفات وتجهيز الـ DataFrames.
* **NumPy:** للعمليات الرياضية والتعامل مع الـ Arrays.
* **Matplotlib & Seaborn:** تم استدعاؤهم عشان نجهز الـ Environment للـ Data Visualization.
* **Missingno:** مكتبة ممتازة استخدمناها عشان نعمل Visualizing للـ Missing Data ونعرف حجم الـ Nulls في كل عمود بوضوح.

---

## 🔄 Data Pipeline & Cleaning Steps (خطوات التنظيف والتجهيز)

مشينا في النوت بوك ده على خطوات منظمة لتنظيف البيانات:

1. **Exploring Columns:** استعرضنا أسماء الأعمدة وحولناها لـ List عشان نفهم الـ Features المتاحة عندنا.
2. **Dropping Unnecessary Features:** شيلنا الـ `Accident_Index` والأعمدة اللي مش هتدخل في التحليل الأساسي أو اللي فيها نسبة Missing Values عالية جداً لا يمكن تعويضها زي `Carriageway_Hazards`, `Time`, و `Police_Force` عشان نخلي الـ Dataset خفيفة ومحددة.
3. **Handling Data Types:** لاحظنا إن عمود التاريخ `Accident Date` كان مقروء كـ `object` (Text)، وحولناه لـ `datetime64` عشان نقدر نعمل Time-Series Analysis بشكل صح قدام.
4. **Investigating Missing Values:** عملنا Check على الـ Null values باستخدام `.isnull().sum()` وعرفنا الأماكن اللي محتاجة معالجة (زي الـ `Weather_Conditions` والـ `Road_Type`).
5. **Statistical Summary:** استخدمنا `.describe()` على الأعمدة الـ Categorical عشان نعرف الـ `top` والـ `freq` لكل ظاهرة (زي إن معظم الحوادث بتتم في الـ Single carriageway وفي جو Fine no high winds).

---

## 📊 Quick Insights from Data Summary
* **حجم البيانات:** بعد التنظيف أصبح معانا **102,657 صف** و **17 عمود**.
* **أكثر نوع طريق متكرر:** هو الـ *Single carriageway*.
* **حالة الطقس الأكثر شيوعاً وقت الحوادث:** الجو الطبيعي المعتدل (*Fine no high winds*).

---

## 🚀 How to Run
تقدر تفتح المشروع وتجربه مباشرة من خلال الضغط على الـ Badge الموجود فوق في النوت بوك:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AbdulrahmanAhmed123/Acceidant-RoadAnalyst/blob/main/Root_cause_accident.ipynb)
