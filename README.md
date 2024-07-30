# E-Commerce Store Sales Analysis - README

## Overview

This project provides a comprehensive analysis of sales data for an e-commerce store. The analysis covers various aspects such as sales, revenue, major products, and key cities contributing to sales and revenue. The dataset used is real and unique, and the analysis is performed using MySQL for querying the data and Power BI for visualization.

## Features

- **Sales and Revenue Analysis:** Detailed examination of sales and revenue trends over time.
- **Product Analysis:** Identification of major products contributing to sales and revenue.
- **Geographical Analysis:** Insights into key cities driving sales and revenue.
- **Interactive Dashboards:** User-friendly Power BI dashboards for exploring the data.

## Installation

### Prerequisites

Ensure you have the following installed:

- MySQL Server
- MySQL Workbench (optional, for query writing)
- Microsoft Power BI Desktop

## Usage

### Setting Up the Database

1. **Create Database:**
   - Open MySQL Workbench and connect to your MySQL Server.
   - Create a new database for the e-commerce sales data:
     ```sql
     CREATE DATABASE ecommerce_sales;
     ```

2. **Import Data:**
   - Import your dataset into the created database. You can use MySQL Workbench or any other tool for importing data from a CSV or Excel file.

### Querying Data with MySQL

1. **Connect to Database:**
   - Open MySQL Workbench and connect to the `ecommerce_sales` database.
   
2. **Write Queries:**
   - Example queries to extract necessary data:
     ```sql
     -- Total Sales and Revenue
     SELECT OrderDate, SUM(TotalAmount) as Revenue, COUNT(OrderID) as Sales
     FROM orders
     GROUP BY OrderDate;

     -- Major Products
     SELECT ProductName, SUM(Quantity) as TotalSold, SUM(TotalAmount) as Revenue
     FROM orders
     GROUP BY ProductName
     ORDER BY Revenue DESC
     LIMIT 10;

     -- Key Cities
     SELECT City, SUM(TotalAmount) as Revenue, COUNT(OrderID) as Sales
     FROM orders
     GROUP BY City
     ORDER BY Revenue DESC
     LIMIT 10;
     ```

### Connecting MySQL to Power BI

1. **Open Power BI Desktop.**
2. **Get Data:**
   - Click on `Home` > `Get Data` > `More...`
   - Select `MySQL database` and click `Connect`.
   
3. **Enter Database Details:**
   - Server: `<your_mysql_server>`
   - Database: `ecommerce_sales`
   
4. **Load Data:**
   - Select the tables or views created from your queries and load them into Power BI.

### Creating Reports

1. **Sales and Revenue Analysis:**
   - Create line charts and bar charts to visualize sales and revenue trends over time.
   
2. **Product Analysis:**
   - Create visuals such as bar charts to highlight top-selling products and their revenue contributions.

### Example Visualizations

- **Sales and Revenue Over Time:**
  - Line chart showing the trend of sales and revenue over time.
  
- **Top Products:**
  - Bar chart displaying the top 10 products by revenue.
  
- **Sales by City:**
  - Map visualization showing sales distribution across different cities.

### Publishing Reports

1. **Save your Power BI report (.pbix file).**
2. **Publish to Power BI Service:**
   - Click on `Home` > `Publish`.
   - Sign in to your Power BI account and publish the report to your workspace.
   
3. **Share and Collaborate:**
   - Share the published report with your team and collaborate on insights.

## Project Structure

- **Power BI Report:** The Power BI Desktop file (.pbix) containing the analysis visualizations.
- **Dataset:** The e-commerce sales data file used for analysis (not included in the repository for privacy reasons).

## Contributing

We welcome contributions to this project. To contribute:

1. Fork the repository.
2. Create a new branch for your feature or improvement.
3. Commit your changes and push the branch.
4. Create a pull request describing your changes.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Contact

For any questions or feedback, please contact aniketdesh004@gmail.com.

---

Thank you for using the E-Commerce Store Sales Analysis tool! Happy analyzing!
