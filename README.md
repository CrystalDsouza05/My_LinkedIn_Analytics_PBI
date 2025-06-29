![image](https://github.com/user-attachments/assets/0d886a80-6fa7-4cae-8a5c-0433f8652754)

# 📊 LinkedIn Data Analytics Dashboard – Power BI Project

Welcome to my Power BI project where I analyzed my personal LinkedIn activity using data exported directly from my profile. This dashboard offers insights into engagements, followers, messaging, invitations, and connections — all visualized through a custom-designed and interactive layout.

---

## 🎯 Objective

To transform raw LinkedIn data into an insightful, interactive, and visually compelling Power BI dashboard that highlights professional growth, engagement patterns, and content performance.

---

## 📁 Data Sources

1. **LinkedIn Data Archive**\
   → *Settings & Privacy > Data Privacy > Get a copy of your data*

2. **Content Performance (Excel Export)**\
   → *Profile > Analytics > Post Impressions > Export File*

---

## 🩹 Data Preparation

- Cleaned and transformed data in Excel and Power Query.
- Built a centralized **Dates** table to support time intelligence.
- Structured the model by separating tables based on purpose for clean flow:
  - `Connections`
  - `Engagement`
  - `Followers`
  - `Invitations`
  - `Messages`
  - `Reactions`
  - `Top Posts Engagement`
  - `Top Posts Impressions`
  - `Dates`

---

## 🧫 Key DAX Measures

```DAX
Invitations Received = COUNTROWS(FILTER(ALL(invitations), Invitations[Direction] = "INCOMING"))
Invitations Sent = COUNTROWS(FILTER(ALL(invitations), Invitations[Direction] = "OUTGOING"))

Msgs Received = CALCULATE(COUNT(messages[FROM]), NOT(messages[FROM] IN { "Crystal Andrea Dsouza" }))
Msgs Sent = CALCULATE(COUNTA(messages[FROM]), FILTER(messages, messages[FROM] = "Crystal Andrea Dsouza"))

Total Companies = DISTINCTCOUNT(Connections[Company])
Total Connections = COUNT(Connections[First Name])
Total Engagement = SUM(Engagement[Engagements])
Total Followers = SUM(Followers[New followers])
Total Impressions = SUM(Engagement[Impressions])
Total Reactions = COUNT(Reactions[Type])
```

---

## 📊 Dashboard Visuals

Here are the key visuals created in Power BI:

### 🔹 KPIs

- Total Engagement
- Total Followers
- Total Connections
- Total Companies
- Total Impressions
- Total Reactions

### 📈 Line & Bar Charts

- Total Engagement and Connections by Month
- Total Impressions by Date

### 🥧 Pie Charts

- Invitations Sent vs Received
- Messages Sent vs Received

### 📊 Bar Chart

- Total Connections by Company

### ☁️ Word Cloud

- Total Connections by Position

### 📋 Table

- Total Reactions by Type (with emojis)

---

## 💡 Features & Interactions

- **Dynamic year filter slicer** (2023, 2024, 2025)
- **Interactive bookmarks** for:
  - Information tooltips
  - Reset view
- **Click-to-filter** capability (e.g. filtering by bar charts)
- **Custom UI Design**: All UI elements styled and conceptualized in **Figma** and **PowerPoint**

---

## 🖼️ Preview

### 📊 Dashboard Overview

![Screenshot 2025-06-28 171151](https://github.com/user-attachments/assets/d49382b6-d1f9-42ca-8fcd-ea3b1eaee066)
![Screenshot 2025-06-28 171231](https://github.com/user-attachments/assets/eeb995af-4a0c-4ea9-bdb4-f6d43ccc20e5)
![Screenshot 2025-06-28 171324](https://github.com/user-attachments/assets/1b04183e-fb44-450c-8871-585bd52de830)
![Screenshot 2025-06-28 171102](https://github.com/user-attachments/assets/dc647f11-ea69-4be7-85bb-41eb00c35d41)

### 🧹 Data Model

![Screenshot 2025-06-28 171530](https://github.com/user-attachments/assets/96ef8140-5793-4ff5-b4ad-6ad31e26af49)


## Background and Information window

Figma
![DASHBOARD (9)](https://github.com/user-attachments/assets/59f76b7e-5581-4382-9895-0b36c8003be3)

PowerPoint
![Picture2](https://github.com/user-attachments/assets/dca6fd01-4ff6-4976-8249-0d841971a715)

---

## 🛠️ Tools Used

- **Power BI** – Data Modeling, DAX, Visualization
- **Microsoft Excel** – Initial Data Cleaning
- **Figma** & **PowerPoint** – Custom UI and layout design
- **GitHub** – Version control & documentation

## Colour Palette Used
![image](https://github.com/user-attachments/assets/00468096-9dd9-426c-b255-a97e259cfb75)

---

## 📬 Contact

Made with ❤️ by **Crystal Andrea Dsouza**\
Let’s [connect on LinkedIn](https://www.linkedin.com/in/crystal-andrea-dsouza-641196286/) and talk dashboards!

