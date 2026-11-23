# Seattle Airbnb Market Analysis (Tableau Portfolio)

> **Note:** This repository compiles my hands-on **Data Analyst practice** in **Tableau Public** using the Seattle Airbnb dataset. It serves as an ongoing case study showcasing multi-dashboard visual exploration across pricing, inventory supply, host performance, booking policies, and seasonal demand.

---

### 📂 Dataset Overview (`Airbnb_Seattle.xlsx`)
This analysis uses the **Seattle Airbnb Open Data** workbook (`Airbnb_Seattle.xlsx`), which captures short-term rental listings, daily availability/pricing schedules, and guest review activity across Seattle, Washington:

* **`Listings` Table:** Property-level attributes including location (`Zipcode`), property and room types (*House, Apartment, Condominium, Townhouse* / *Entire home/apt, Private room, Shared room*), bedroom counts, nightly base prices, booking policies (*Instant Bookable*, *Cancellation Policy*), and host status (*Superhost* vs. *Regular Host*).
* **`Calendar` Table:** Date-level pricing and availability records spanning **2016–2017**, enabling weekly revenue tracking and seasonal availability comparisons.
* **`Reviews` Table:** Guest review counts and satisfaction scores grouped into performance tiers (*Elite*, *Great*, *Needs Work*, *No Review*) to evaluate how reputation impacts pricing.

---

### 📁 Repository Contents
* **`Airbnb_Seattle.xlsx`:** Source Excel workbook containing the `Listings`, `Calendar`, and `Reviews` tables used for data blending and visualization.
* **`dashboard1.png` & `dashboard2.png`:** High-resolution exports of both interactive Tableau dashboards.
* **`README.md`:** Dataset documentation, dashboard purposes, live Tableau Public links, and analytical insights.

---

### 📊 Dashboard 1: Pricing, Supply & Annual Revenue
🔗 **[View Interactive Dashboard 1 on Tableau Public](https://public.tableau.com/app/profile/efren.lamoste/viz/SeattleAirbnbPricingSupplyAnnualRevenue/Dashboard1)**

![Seattle Airbnb Dashboard 1](./dashboard1)

#### **Purpose**
Provide prospective Airbnb hosts and real estate investors with a clear market baseline—answering **how much properties charge by size and neighborhood**, **where market supply is concentrated**, and **how total revenue fluctuates across the calendar year**.

#### **Key Insights**
* **Price Scaling by Property Size (`Avg Price Per Bedroom`):** Nightly rates increase steadily with bedroom count—starting at **$96.2** for 1-bedroom units, **$175.4** (2 BR), **$249.7** (3 BR), **$315.4** (4 BR), **$450.0** (5 BR), and reaching **$584.8** for 6-bedroom properties.
* **Market Supply Distribution (`Distinct Count of Bedroom Listings`):** 1-bedroom units dominate Seattle's inventory with **1,811 listings**, followed by 2-bedroom (**483**) and 3-bedroom (**206**) units, while 5- and 6-bedroom homes remain scarce (**20** and **5** listings).
* **Neighborhood Pricing (`Price for Zipcode` & `Price by Zipcode`):** Central and waterfront zip codes command premium rates led by **98134 ($206.6)**, **98119 ($171.1)**, and **98101 ($166.9)**—whereas outer residential zones like **98125 ($64.7)** offer the most budget-friendly rates.
* **Annual Revenue Trajectory (`Revenue for Year`):** Weekly calendar revenue climbs sharply from roughly **$1,000K** in early January to over **$2,000K** by late spring and remains strong through year-end.

---

### 📊 Dashboard 2: Host Performance, Booking Policies & Property Types
🔗 **[View Interactive Dashboard 2 on Tableau Public](https://public.tableau.com/app/profile/efren.lamoste/viz/SeattleAirbnbHostPerformanceBookingPoliciesPropertyTypes/Dashboard2)**

![Seattle Airbnb Dashboard 2](./dashboard2)

#### **Purpose**
Help existing and new hosts optimize their listing strategy—evaluating **how cancellation and instant-booking policies affect pricing across seasons**, **which property/room configurations face the highest competition**, and **whether earning Superhost status translates into higher nightly rates**.

#### **Key Insights**
* **Booking Policies & Seasonal Availability:** Listings enforcing **strict cancellation policies** command noticeably higher average nightly rates across both **2016** and **2017** (peaking around **$156–$161** under Instant Booking) compared to moderate and flexible policies.
* **Property & Room Type Competition:** Across all major property categories (*House, Townhouse, Condominium, Apartment*), **Entire home/apt** listings command the highest rates—led by Houses (**$192.1** avg) and Townhouses (**$184.7** avg)—while **Apartments** represent the largest supply volume (**406,905** calendar entries).
* **Superhost vs. Regular Host Pricing Assessment:** *Superhosts* consistently achieve higher nightly averages within comparable review tiers (such as **$153.38** vs. **$120.23** in the *Great* review score group), demonstrating the pricing power of verified host reputation.

---

### 🛠️ Tools & Tableau Features Used
* **Visualization Tool:** Tableau Public
* **Chart Types:** Filled Geospatial Maps (`Zipcode`), Grouped & Ranked Bar Charts, Summary Tables (`COUNTD`), and Continuous Line Charts (`Week of Date`)
* **Techniques:** Multi-table data blending (`Listings`, `Calendar`, `Reviews`), calculated fields/grouping (`Review score group`), and multi-panel dashboard composition
