# Pizza Sales Data Analysis

Welcome to the Pizza Sales Data Analysis project! In this repository, you'll find the necessary files to replicate the analysis conducted on pizza sales data using MySQL.

## Files Included

- `Pizza Sales Data Analysis.sql`: MySQL script containing the analysis queries.
- `dataset/`:
  - `order_details.csv`: CSV file containing order details.
  - `orders.csv`: CSV file containing order information.
  - `pizza_types.csv`: CSV file containing pizza types.
  - `pizzas.csv`: CSV file containing pizza details.

## Setup Instructions

Follow these steps to set up the MySQL database and run the analysis:

1. **Download the Repository**:
   - Clone this repository to your local machine:
     ```sh
     git clone https://github.com/karstendsouza/Pizza-Sales-Data-Analysis.git
     cd Pizza-Sales-Data-Analysis
     ```

2. **MySQL Database Setup**:
   - Open MySQL Workbench (or any MySQL client).
   - Create a new database:
     ```sql
     CREATE DATABASE pizzahut;
     USE pizzahut;
     ```

3. **Importing the Dataset**:
   - Use the MySQL Workbench to import the CSV files into their respective tables:
     - `pizzas.csv` -> `pizzas` table
     - `pizza_types.csv` -> `pizza_types` table
     - Manually create the `orders` table:
       ```sql
       CREATE TABLE orders (
           order_id INT NOT NULL,
           order_date DATE NOT NULL,
           order_time TIME NOT NULL,
           PRIMARY KEY (order_id)
       );
       ```
       Import `orders.csv` into the `orders` table.
     - Manually create the `order_details` table:
       ```sql
       CREATE TABLE order_details (
           order_details_id INT NOT NULL,
           order_id INT NOT NULL,
           pizza_id TEXT NOT NULL,
           quantity INT NOT NULL,
           PRIMARY KEY (order_details_id)
       );
       ```
       Import `order_details.csv` into the `order_details` table.

4. **Running the Script**:
   - Open `Pizza Sales Data Analysis.sql` in MySQL Workbench.
   - Ensure you're connected to the `pizzahut` database.
   - Run the entire script.

## Key Insights

Here are some key insights from the analysis:
- Total Orders & Revenue: 21,350 orders, generating $817,860.05 revenue.
- Most Expensive Pizza: Greek Pizza at $35.95.
- Popular Pizza Sizes: Large pizzas dominate with 18,526 orders.
- Top 5 Most Ordered Pizzas:
  1. Classic Deluxe Pizza: 2,453 orders
  2. Barbecue Chicken Pizza: 2,432 orders
  3. Hawaiian Pizza: 2,422 orders
  4. Pepperoni Pizza: 2,418 orders
  5. Thai Chicken Pizza: 2,371 orders
- Revenue Leaders:
  - Thai Chicken Pizza: $43,434.25
  - Barbecue Chicken Pizza: $42,768.00
  - California Chicken Pizza: $41,409.50

## Explore Further

Dive deeper into the data and explore the full analysis by running the provided script or visiting the GitHub repository: [Pizza Sales Data Analysis](https://github.com/karstendsouza/Pizza-Sales-Data-Analysis).

## Feedback and Collaboration

I'm open to feedback and collaboration opportunities. Feel free to reach out to karstendsouza@gmail.com with your thoughts or suggestions!

