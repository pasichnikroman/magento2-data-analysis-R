# Magento 2 Data Analysis in R

This project provides an analysis of Magento 2 e-commerce data using R. You will connect to a Magento MySQL database, extract relevant sales and customer data, and perform various analyses to uncover trends and patterns.

## Installation and Setup

### Prerequisites

- Docker
- RStudio Server
- A Magento MySQL Database

### Step 1: Clone the Repository

First, clone this repository to your local machine:

```bash
git clone https://github.com/pasichnikroman/magento2-data-analysis-R
cd magento2-data-analysis-R
```

### Step 2: Run RStudio Server with Docker
Once the repository is cloned, you can run RStudio Server inside a Docker container. Run the following command:

```bash
docker run --net="host" --name rstudio_server -d -v $PWD:/home/rstudio -e PASSWORD=password -t rheartpython/swashbuckling-r
```

This command will:

- Run the RStudio server in a Docker container.
- Mount the current directory (`$PWD`) to the RStudio user's home directory.
- Set a password (`password`) for RStudio Server access.
- Run the container in detached mode (`-d`).


### Step 3: Access RStudio
After running the above command, you can access the RStudio Server in your browser by navigating to:

http://localhost:8787


#### Log in with the following credentials:

Log in with the following credentials:

- **Username**: `rstudio`
- **Password**: `password`

### Step 4: Open and Run the Magento Analysis
In the RStudio interface, navigate to the cloned repository folder and open the magento.qmd file. This file contains the code for connecting to a Magento MySQL database and performing data analysis.

### Step 5: Connect to Magento MySQL Database
Make sure to update the following variables in the code to match your database credentials:

```bash
db_host <- "db_host"
db_user <- "db_user"
db_password <- "db_password"
db_name <- "db_name"
```

### Step 6: Run the Analysis

After making the necessary changes to connect to your database, you can run the analysis directly from RStudio.

In the file `magento.qmd`, you'll find multiple sections performing different analyses:

- **Sales Data Overview**: Fetch and visualize total sales and products sold.
- **Sales Trends**: Visualize daily sales trends.
- **Popular Order Times**: Determine the most common times for customer orders.
- **Sales by Product Category**: Analyze which product categories are generating the most revenue.
- **Customer Segmentation**: Segment customers based on their spending.
- **Customer Locations**: Visualize customer locations on a map using `google maps` and `leaflet`. Change on your api key

