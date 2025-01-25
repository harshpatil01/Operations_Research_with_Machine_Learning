
# **Optimal Inventory Control Using Linear Programming**

## **Project Overview**
This project showcases an optimal inventory control system using **Linear Programming**. The goal is to minimize the total cost of inventory management for multiple products by balancing **ordering costs**, **holding costs**, and **demand variability**. The project utilizes real-world sales and inventory data for four products:
- **Berry Juice**
- **Mango Smoothie**
- **Apple Cider**
- **Orange Soda**

The project is implemented in Python, leveraging optimization libraries and data visualization techniques.

---

## **Key Features**
1. **Data Preprocessing**: 
   - Organized 100 months of inventory data for four products.
   - Ensured each product had attributes like demand, storage capacity, and initial inventory levels.

2. **Optimization**: 
   - Developed a mathematical model using **Linear Programming** to minimize the total cost of inventory control.
   - Costs included:
     - **Ordering Costs**: Cost incurred for replenishing stock.
     - **Holding Costs**: Cost of maintaining stock in inventory.
   - Solved the problem using the **`cvxpy`** library.

3. **Visualization**:
   - Generated insightful visualizations to compare:
     - **Monthly Demand vs. Order Quantities**
     - **Inventory Trends vs. Storage Capacity**

4. **Results Export**:
   - Consolidated the optimized results into a CSV file for further analysis or reporting.

5. **Presentation**:
   - Summarized findings and visualizations into a professional PowerPoint presentation.

---

## **Steps Followed**

### 1. **Dataset Preparation**
   - Collected and formatted monthly sales and inventory data for four products.
   - Key attributes:
     - **Month**: Time period (1–100).
     - **Demand**: Monthly customer demand.
     - **Storage Capacity**: Maximum inventory that can be held.
     - **Initial Inventory**: Starting stock at the beginning of the time period.

### 2. **Mathematical Model Formulation**
   - Decision variables:
     - \( x_t \): Order quantity for month \( t \).
     - \( I_t \): Inventory level at the end of month \( t \).
   - Objective function:
     - Minimize \( 	ext{Total Cost} = c_o \cdot x_t + c_h \cdot I_t \), where:
       - \( c_o \): Ordering cost per unit.
       - \( c_h \): Holding cost per unit per month.
   - Constraints:
     - Inventory levels must remain non-negative.
     - Inventory cannot exceed storage capacity.
     - Demand must be met for each month.

### 3. **Optimization Implementation**
   - Used **`cvxpy`** to solve the optimization problem for each product.
   - Calculated:
     - Optimal order quantities for each month.
     - Ending inventory levels for each month.
     - Total cost of inventory management for each product.

### 4. **Visualization**
   - Created charts for each product using **Matplotlib**:
     - **Demand vs. Order Quantities**: Illustrates alignment of order quantities with demand.
     - **Inventory Trends**: Highlights adherence to storage capacity constraints.

### 5. **Export Results**
   - Exported consolidated results into a CSV file:
     - Columns: Month, Demand, Order Quantity, Ending Inventory, Total Cost.

### 6. **Presentation**
   - Compiled key insights and visualizations into a professional PowerPoint presentation.
   - Highlighted efficiency gains, cost savings, and operational improvements.

---

## **Technologies Used**
- **Python Libraries**:
  - `cvxpy`: For linear programming and optimization.
  - `pandas`: For data manipulation.
  - `matplotlib`: For data visualization.
  - `pptx`: For automating PowerPoint presentation updates.
- **Microsoft Excel**: For dataset preparation.
- **Microsoft PowerPoint**: For results presentation.

---

## **How to Run the Project**

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/optimal-inventory-control.git
   cd optimal-inventory-control
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Analysis**
   - Open the Jupyter Notebook:
     ```bash
     jupyter notebook inventory_control.ipynb
     ```
   - Run all cells to execute the analysis and generate results.

4. **Export Results**
   - After running the notebook, find the optimized results in `optimal_inventory_control_results.csv`.

5. **View Presentation**
   - Open `Updated_Optimal_Inventory_Control_Presentation.pptx` to see the summarized results and insights.

---

## **Project Structure**
```
optimal-inventory-control/
├── data/
│   ├── Final_Inventory_Adjusted_Months.xlsx      # Processed dataset
├── notebooks/
│   ├── inventory_control.ipynb                  # Jupyter Notebook for analysis
├── results/
│   ├── optimal_inventory_control_results.csv    # Exported results
├── presentation/
│   ├── Updated_Optimal_Inventory_Control_Presentation.pptx  # Final presentation
├── visuals/
│   ├── [Product]_Demand_vs_Order.png            # Demand vs. Order chart for each product
│   ├── [Product]_Inventory_Levels.png           # Inventory trend chart for each product
├── requirements.txt                             # Required Python libraries
└── README.md                                    # Project documentation
```

---

## **Key Insights**
1. **Cost Efficiency**:
   - Reduced overall ordering and holding costs.
   - Achieved a balance between inventory levels and demand fulfillment.

2. **Operational Improvements**:
   - Met demand requirements consistently across all products.
   - Ensured smooth supply operations and avoided overstocking.

3. **Scalability**:
   - The optimization framework is adaptable for additional products and larger datasets.

---

## **Acknowledgments**
- **Dataset Source**: Kaggle Sales and Inventory Dataset ([link](https://www.kaggle.com/datasets/yukisim/sales-and-inventory-dataset/data))
- **Libraries Used**: `cvxpy`, `matplotlib`, `pandas`, `pptx`
