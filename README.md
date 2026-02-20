# Victoria Secret Facility Manager
A retail analytics and workforce migration suite designed to manage existing facilites and strategic expansion. This solution integrates a Python-powered 50,000-employee simulation with Power BI geospatial revenue modeling to bridge the gap between human capital and real estate profitability.

**Tech Stack**
- **Power BI**: Relational modeling, Geospatial visualization, DAX, and custom brand-aligned UI/UX.
- **Python (Pandas/NumPy)**: Automated generation of 50k+ unique employee records and multi-sheet Excel manipulation.

**Key Features**

### Strategic Growth & Revenue Modeling
- **Dynamic Potential Profit**: A Rank-based growth chart that visualizes the "Profit Climb,"Rank 1 (Current) stores against the estimated revenue of Proposed locations (Ranks 2-5).
- **Expansion Slicers**: Interactive "Rank" and "Division Strategy" filters that allow executives to simulate the financial impact of opening new locations.
- **Brand Identity**: Custom UI utilizing high-contrast pink and charcoal themes to mirror the professional, editorial aesthetic of a luxury global brand.

### Geospatial Market Intelligence
- **(Future) Locations Map**: Real-world NYC Latitude/Longitude plotting that visualizes the current retail footprint across Manhattan, Brooklyn, and Queens.
- **Assessment Mapping**: Identification of high-value corridors through color-coded status bubbles (Active vs. Proposed).

### Advanced Workforce Matrix & Capacity Logic
- **Location Occupancy Matrix**: A comprehensive migration tool that cross-references `Current Facility` against `Future Facility` to predict staff flows.
- **Capacity Guardrails**: Integrated vacancy logic at the bottom of the matrix showing "Total Employees," "Future Capacity," and "Vacancies" to prevent site over-saturation.
- **Departmental Segmentation**: Real-time visibility into specific units (Swimsuits, Sweatsuits, Mens, etc.) to ensure balanced distribution across the 20 current and 10 proposed sites.

**Data Architecture**
The app utilizes a centralized `VS_Data.xlsx` engine with a 1:Many relational structure:
- **Active_Directory**: 50,000 records mimicking an enterprise environment with unique titles and departments.
- **Store_Locations**: Geospatial master list containing Site Rank, Status, and Estimated Profit.
- **Work_Unit**: A hierarchy covering Apparel, Intimates, Mens, Accessories, and Corporate.
- **Moving_Table**: The logic-gate for staff migration and facility vacancy forecasting.

- ## How to Use
To explore this analytics solution locally:
1. **Download the Dataset**: Download the `VS_Data.xlsx` file from this repository.
2. **Download the Power BI File**: Download the `.pbix` file.
3. **Connect the Data**: Open the Power BI file. If prompted for a data source, point the connection to the location of the downloaded Excel file on your machine.

> [!WARNING]
> Data used is NOT REAL
