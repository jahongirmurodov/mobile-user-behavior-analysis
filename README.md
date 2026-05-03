# Mobile User Behavior Analysis

## Overview
This project focuses on analyzing user activity and behavior in mobile applications. The goal was to identify patterns in user engagement, device usage, and resource consumption, as well as to provide insights for improving user experience (UX) and retention.

## Problem Statement
Mobile application datasets often contain complex behavioral patterns influenced by multiple factors such as device type, operating system, age, and usage habits. The objective of this project was to clean the data, perform exploratory analysis, and identify key drivers of user activity, battery consumption, and data usage.

## Objectives
- Perform data cleaning and preprocessing  
- Conduct exploratory data analysis (EDA)  
- Analyze user behavior patterns  
- Identify relationships between key metrics  
- Segment users based on activity and demographics  
- Generate insights for product improvement  

## Tech Stack
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

## Data Description
The dataset contains information about mobile users and their behavior:

- User ID  
- Device Model  
- Operating System (Android / iOS)  
- App Usage Time (min/day)  
- Screen On Time (hours/day)  
- Battery Drain (mAh/day)  
- Number of Apps Installed  
- Data Usage (MB/day)  
- Age  
- Gender  
- User Behavior Class (1–4)  

## Methodology

### 1. Data Preprocessing
- Loaded dataset into Pandas DataFrame  
- Checked for missing values, duplicates, and data types  
- Filled missing values:
  - Numerical → median  
  - Categorical → "Unknown"  
- Converted data types where necessary  

#### Feature Engineering:
- `AppUsageHours = App Usage Time / 60`  
- `BatteryDrainPerHour = Battery Drain / Screen On Time`  
- `AppsPerHour = Number of Apps Installed / Screen On Time`  

---

### 2. Exploratory Data Analysis (EDA)

#### Usage Analysis
- Distribution of App Usage Time  
- Relationship with:
  - Age  
  - Gender  
  - Operating System  
  - Number of installed apps  

#### Screen Time Analysis
- Boxplot of Screen On Time by OS  
- Correlation between Screen On Time and Battery Drain  

#### Battery Analysis
- Correlation heatmap for Battery Drain  
- Top 5 device models with highest battery consumption  

#### Apps Analysis
- Impact of number of apps on:
  - Battery usage  
  - Data usage  
  - App usage time  

#### Data Usage Analysis
- Relationship between Data Usage and App Usage Time  
- Outlier detection using boxplots  

---

### 3. User Behavior Analysis

- Distribution of users across behavior classes  
- Average metrics per class:
  - App Usage Time  
  - Battery Drain  
  - Number of Apps  
  - Data Usage  

#### Visualizations:
- Barplot of average App Usage Time by class  
- Barplot of average Battery Drain by class  

#### Activity Segmentation:
- Created "Activity Level":
  - <200 → Low  
  - 200–350 → Medium  
  - >350 → High  

- Visualized distribution of activity levels  

---

### 4. Correlation Analysis
- Built correlation matrix for numerical features  
- Visualized using heatmap  

#### Key relationships analyzed:
- App Usage Time ↔ Data Usage  
- Screen On Time ↔ Battery Drain  
- Age ↔ App Usage Time  

---

### 5. User Segmentation

#### Segmentation Criteria:
- Age groups:
  - 10–20  
  - 21–30  
  - 31–40  
  - 41–50  
  - 51+  

- Activity level (Low / Medium / High)  
- Operating System (Android / iOS)  

#### Comparison Metrics:
- Average App Usage Time  
- Average Battery Drain  
- Average number of installed apps  

---

### 6. Visualizations
The project includes multiple visualizations:
- Histograms (distributions)  
- Boxplots (group comparison & outliers)  
- Barplots (averages)  
- Scatterplots (relationships)  
- Heatmaps (correlations)  

---

## Results & Insights
- Identified key factors affecting user activity  
- Observed strong relationship between screen time and battery drain  
- Higher app usage leads to increased data consumption  
- User activity varies significantly across behavioral classes  
- Device type and OS influence usage patterns  

---

## Key Takeaways
- User behavior is influenced by multiple interacting factors  
- Feature engineering improves analytical depth  
- Segmentation helps identify high-value user groups  
- Data-driven insights can support UX improvements  

---

## Possible Improvements
- Apply clustering algorithms for advanced segmentation  
- Build predictive models (user activity prediction)  
- Create interactive dashboards (Power BI / Tableau)  
- Detect anomalies using statistical methods (IQR)  

---

# Анализ поведения пользователей мобильных приложений

## Обзор проекта
Проект посвящен анализу пользовательской активности в мобильных приложениях. Цель — выявить закономерности поведения пользователей, а также факторы, влияющие на использование приложений, расход батареи и интернет-трафик.

## Постановка задачи
Поведение пользователей зависит от множества факторов: устройства, ОС, возраста и привычек. Необходимо очистить данные, провести анализ и выявить ключевые зависимости.

## Цели проекта
- Очистка и подготовка данных  
- Проведение EDA  
- Анализ пользовательского поведения  
- Поиск взаимосвязей между метриками  
- Сегментация пользователей  
- Формирование инсайтов  

## Используемые технологии
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

## Описание данных
Датасет содержит:

- ID пользователя  
- Модель устройства  
- Операционная система  
- Время использования приложений  
- Время экрана  
- Расход батареи  
- Количество приложений  
- Интернет-трафик  
- Возраст  
- Пол  
- Класс поведения пользователя  

## Методология

### 1. Предобработка данных
- Проверка пропусков и дубликатов  
- Обработка пропусков  
- Приведение типов данных  

#### Созданные признаки:
- AppUsageHours  
- BatteryDrainPerHour  
- AppsPerHour  

---

### 2. Анализ данных
- Анализ времени использования  
- Анализ экранного времени  
- Анализ батареи  
- Анализ приложений  
- Анализ интернет-трафика  

---

### 3. Анализ поведения пользователей
- Распределение по классам  
- Средние показатели по классам  
- Визуализация метрик  

#### Сегментация активности:
- Low / Medium / High  

---

### 4. Корреляционный анализ
- Корреляционная матрица  
- Heatmap  
- Анализ ключевых зависимостей  

---

### 5. Сегментация пользователей
- По возрасту  
- По активности  
- По ОС  

Сравнение:
- Время использования  
- Расход батареи  
- Количество приложений  

---

## Результаты
- Выявлены факторы, влияющие на активность пользователей  
- Найдена связь между экранным временем и расходом батареи  
- Обнаружена зависимость между использованием приложений и трафиком  
- Определены активные группы пользователей  

## Выводы
- Поведение пользователей зависит от множества факторов  
- Сегментация помогает лучше понять аудиторию  
- Анализ данных может улучшить UX и retention  

## Возможные улучшения
- Кластеризация пользователей  
- Построение ML-моделей  
- Создание дашборда  
- Поиск аномалий  
