# FitLife Hub – Fitness & Lifestyle Monitoring Database System

FitLife Hub is a database-driven fitness and lifestyle monitoring system designed to help users track physical activity, nutrition intake, and overall health progress. The system integrates relational and NoSQL databases with analytics to provide meaningful insights into user health behavior.

The platform allows users to monitor workouts, calories burned, nutrition intake, water consumption, and fitness goals while enabling interaction with fitness coaches, doctors, and dieticians for guidance.

Project Report: :contentReference[oaicite:0]{index=0}

---

## Project Overview

Modern lifestyles often lead to sedentary habits, unhealthy eating patterns, and reduced physical activity. FitLife Hub addresses this challenge by providing a centralized system that tracks and analyzes user health data to promote healthier living.

The system includes features for:

- Activity tracking (walking, cycling, swimming, workouts)
- Nutrition and water intake monitoring
- BMI tracking and fitness goal setting
- Social interaction among users
- Medical and dietary consultation support for premium users

The database architecture integrates **MySQL for relational data management**, **MongoDB for NoSQL storage**, and **Python for analytics and visualization**.

---

## System Architecture

The system is designed using both **Relational Database Modeling and NoSQL modeling**.

Key design components include:

- **EER Diagram** representing entities such as Users, Activities, Nutrition Tracker, and Administrators  
- **UML Diagram** defining object relationships and system interactions  
- **Relational Schema Mapping** with primary and foreign key constraints

The EER and UML diagrams defining these relationships are shown in the project report (pages 4–5). :contentReference[oaicite:1]{index=1}

---

## Database Design

The relational database includes entities such as:

- User
- Premium User
- General User
- Activity Tracker
- Nutrition Tracker
- Daily Intake
- Water Intake
- Administrator
- Fitness Coach
- Medical Counselling
- Payment
- Goal Setting

These tables are linked using **primary and foreign key relationships** to ensure data integrity and efficient querying. :contentReference[oaicite:2]{index=2}

---

## MySQL Implementation

The relational model was implemented in **MySQL** and several analytical queries were executed, including:

- Identifying users who performed specific activities (e.g., cycling)
- Finding users who consumed the highest water intake
- Calculating total calories burned by users per activity
- Identifying users without payment details
- Detecting users whose calories burned exceeded the average

Example SQL query:

```sql
SELECT A.Activity_type, U.User_Name, A.Calories_burnt, A.Distance_covered
FROM activity_tracker A
INNER JOIN User U ON U.User_Id = A.User_Id
WHERE A.Activity_type = 'CYCLING';
