# VS Global Retail & Staffing Analytics (Bathing Suit Division)
A comprehensive data analytics solution designed to visualize Victoria's Secret retail performance and staff movement, utilizing Python for high-volume synthetic data generation (50k+ records) and Power BI for relational modeling, capacity forecasting, and geospatial insights.

**Tech Stack**
- **Power BI**: Relational modeling (Star Schema), DAX vacancy measures, and Geospatial ranking.
- **Python (Pandas/NumPy)**: Automated generation of Active Directory datasets and multi-sheet Excel manipulation.

**Key Features**

### Geospatial Store Ranking & Profit Analytics
- **Rank-Based Mapping**: Visualizes store locations globally, categorized by performance ranks (1-5) to identify high-value hubs.
- **Profit Scalability Chart**: A dynamic line chart showing the "Rank Up" effect—predicting revenue increases when proposed locations move to active status.
- **Site Status Slicers**: Toggle between Active, Proposed, and Decommissioned retail sites.

### Organizational Matrix & Staffing Modeling
- **50,000 Employee Simulation**: Python-generated Active Directory mimicking a real-world enterprise environment including unique IDs, titles, and department hierarchies.
- **Work Unit Synchronization**: A lookup table architecture that ensures 100% alignment between HR departments and physical work units.
- **Employee Type Segmentation**: Analysis of Full-Time vs. Part-Time distribution across global locations.

### Predictive Facility & Vacancy Analysis
- **The "Moving Table" Logic**: Tracks the scheduled migration of staff from current facilities to future locations/floors.
- **Capacity vs. Future Total**: A Matrix visual that calculates future headcount against facility limits to identify "at-capacity" risks.
- **Dynamic Vacancy Measure**: Custom DAX formulas that subtract "Movers" from "Future Capacity" to provide real-time seating availability counts.

---

## Data Structure
The app utilizes a centralized `VS_Data.xlsx` file generated via Python with the following architecture:

| Sheet Name | Purpose | Key Fields |
| :--- | :--- | :--- |
| **Store_Locations** | Map & Profit Data | SiteId, Rank, EstProfitIncrease |
| **Active_Directory** | Employee Fact Table | Email, Department, StreetAddress |
| **Moving_Table** | Staff Migration Logic | ID, Future Facility, Future Floor |
| **Work_Unit** | HR Dimension Table | DIV, SubDivision, Operations |
| **Facilities_Future** | Capacity Forecasting | FullTimeCapacity, SiteId |
