🏥 Hospital Operations Dashboard — Power BI


A comprehensive multi-page Power BI dashboard analyzing hospital performance across Doctors, Patients, Finance, and Medicine Stock for City General Hospital (2023–2026).

📌 Project Overview

This dashboard was built to give hospital management a 360° operational view — from patient flow and doctor performance to revenue breakdowns and medicine inventory. The goal was to transform raw hospital data into actionable BI insights using Power BI's full stack: data modeling, DAX, Power Query, and interactive UX design.


🖥️ Dashboard Pages

🏠 Home (Landing Page)

Navigation hub with direct links to all four analytical sections — designed for clean, intuitive UX.

👨‍⚕️ Doctor Page


7,000 total appointments tracked
Doctor-wise performance table: Appointments, Billing Amount, Commission, Status (Top Performer / Average)
Appointment split: Online vs Walk-in
Appointment distribution by Specialization (ENT leads at 900)
Doctor Information Card: Profile photo, specialization, experience, qualification, upcoming appointments
Doctor gender distribution


🧑‍🤝‍🧑 Patients Page


5,000 total patients | Avg. Stay: 3.9 Days
Admitted: 640 | Discharged: 2,571 | Scheduled: 1,474
Patient overview table: Name, Gender, Insurance, Symptoms, Room No., Total Bill
Monthly patient volume trend (Jan–Dec)
Insurance provider breakdown (HDFC Ergo, ICICI Lombard, Star Health, Not Insured)
Age group distribution: Senior Citizen → Adult
Patient Information Card: Photo, blood group, gender, age, diagnosis, rating


💰 Finance Page


Total Revenue: ₹52.89M
KPI Cards: Avg Revenue (10.58K), Room Charge (25.33M), Test Charge (15.98M), Medicine Charge (7.56M), Consultation (6M)
Revenue by Month (line chart with MoM % change annotations)
Revenue by Insurance Provider (bar chart)
Distribution of Revenue by charge type (horizontal bar)
Payment Split donut: Cash (36.19%), Card (28%), UPI (22.95%), Insurance (12.86%)
Medicine heatmap by Day and Month


💊 Stock & Medicines Page


Total Stock Volume: 600.7M | Total Stock: 986.1K | Current Stock: 968.7K
Dispensed Stock: 17.4K | Dispensed Amount: 4.3M
Medicine status table: Name, Type, Dispersed Date, Expiry, Stock QTY, Unit Price
Top dispensed medicines by name (Insulin, Amoxicillin, Ibuprofen lead)
Dispensed QTY by medicine type: Injection, Tablet, Syrup, Capsule (~4.4K each)
Medicine Stock Status donut: Over Stock (11.9K), In Stock (2.8K), Low Stock (2.6K)



🔑 Key Business Insights


📈 Revenue peaks in August (+19.4% MoM) and dips in June–July — potential seasonal patient volume pattern
💳 Cash dominates payments (36.19%) — opportunity to push digital payment adoption
🩺 ENT has the highest appointment load (900) — resource planning needed for staffing
⚠️ Over-stocking is a critical issue — 11.9K units overstocked vs 2.6K low stock, indicating poor inventory planning
🏥 Not Insured patients (13.9M revenue) are the highest revenue segment — pricing strategy review recommended
📊 Avg. stay of 3.9 days with 640 admitted vs 2,571 discharged suggests high throughput but possible readmission risk



🛠️ Tech Stack

ToolUsagePower BI DesktopDashboard development, report designDAXKPI measures, MoM calculations, conditional formattingPower Query (M)Data cleaning, transformation, type correctionData ModelingStar schema, relationship management, cardinality optimizationFigmaUI/UX wireframing before Power BI build


📐 Data Model Highlights


Star schema design with fact tables (appointments, billing, medicine stock) and dimension tables (doctors, patients, dates)
Custom Calendar/Date table for time intelligence measures
Proper cardinality & filter direction setup across all relationships
Resolved many-to-many relationship risks using bridge tables



📊 DAX Measures Used

dax-- MoM Revenue Change %
MoM % Change = 
VAR CurrentMonth = [Total Revenue]
VAR PrevMonth = CALCULATE([Total Revenue], DATEADD(Calender_table[Date], -1, MONTH))
RETURN DIVIDE(CurrentMonth - PrevMonth, PrevMonth, 0)

-- Total Revenue
Total Revenue = SUM(finance[Total_Bill])

-- Avg Stay Days
Avg Stay Days = AVERAGE(patients[Stay_Days])


🗂️ Dataset Overview

TableDescriptionPatientsPatient demographics, symptoms, insurance, billingDoctorsSpecialization, appointments, commission, ratingsFinanceRevenue by charge type, payment method, insuranceMedicinesStock levels, dispensing data, expiry trackingCalendarDate dimension for time intelligence


📝 Dataset is synthetic/fictional, created for portfolio demonstration purposes.


🚀 How to View


Download the .pbix file from this repository
Open in Power BI Desktop (free download from Microsoft)
Navigate using the left sidebar: Home → Doctor → Patients → Finance → Stock & Medicines


👤 About the Author

Shivraj Singh Sisodiya
Aspiring Data Analyst & Power BI Developer | B.Pharm 2027
Contact 9351946674
Email_id shivrajsinghsisodiya9351@gmail.com

🌐 Portfolio: datascienceportfol.io/shivraj
💼 LinkedIn: linkedin.com/in/shivrajsinghsisodiya
🐙 GitHub: github.com/shivrajsinghsisodiya


