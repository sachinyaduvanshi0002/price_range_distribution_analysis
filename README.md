# 🍽️ Price Range Distribution Analysis

## 📊 Cognifyz Technologies Data Analysis Internship

This project is part of the **Cognifyz Technologies Data Analysis Internship Program**.

The objective of this task is to analyze the **distribution of restaurant price ranges** and understand how restaurants are distributed across different price categories.

---

## 🎯 Task Objective

1. Analyze the distribution of **price ranges** among restaurants.
2. Calculate the **percentage of restaurants** in each price range category.
3. Present the findings using SQL queries and data analysis.

---

## 🗂️ Dataset

The dataset contains information about restaurants such as:

* Restaurant Name
* City
* Cuisines
* Aggregate Rating
* Votes
* Price Range
* Online Delivery Availability
* Table Booking Availability

---

## 🛠️ Tools Used

* PostgreSQL
* SQL
* GitHub

---

## 💻 SQL Queries Used

### 1️⃣ Price Range Distribution

```sql
SELECT 
    price_range,
    COUNT(*) AS total_restaurants
FROM restaurants
GROUP BY price_range
ORDER BY price_range;
```

This query counts the number of restaurants available in each price range.

---

### 2️⃣ Percentage of Restaurants in Each Price Range

```sql
SELECT 
    price_range,
    COUNT(*) AS total_restaurants,
    ROUND(
        COUNT(*) * 100.0 / SUM(COUNT(*)) OVER(),
        2
    ) AS percentage
FROM restaurants
GROUP BY price_range
ORDER BY price_range;
```

This query calculates the percentage distribution of restaurants across different price ranges.

---

## 📈 Key Insights

* Most restaurants fall under **Price Range 1**, indicating a large number of affordable dining options.
* Mid-range restaurants (**Price Range 2**) also represent a significant portion.
* Higher price ranges (**3 and 4**) have fewer restaurants compared to lower price ranges.
  
---

<img width="1920" height="1080" alt="Screenshot 2026-03-08 203646" src="https://github.com/user-attachments/assets/cadfbc5f-f80f-46a3-bdc7-ef1f322424d6" />
<img width="1920" height="1080" alt="Screenshot 2026-03-08 203634" src="https://github.com/user-attachments/assets/55b8dacd-c54b-49e7-bf51-4942eb23a31f" />

---
