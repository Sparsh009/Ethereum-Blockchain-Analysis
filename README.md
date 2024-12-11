# Ethereum Blockchain Analysis

## Project Overview
This project aims to analyze Ethereum blockchain data using Apache Spark. The focus is on transactions from August 2015 to January 2019, with detailed analysis on miner activities, block sizes, and transaction fees.

## Dataset Description
The dataset comprises two main CSV files:
- `blocks.csv`: Contains data about the blocks on the Ethereum blockchain.
- `transactions.csv`: Contains details of transactions within those blocks.

## Repository Structure
- `src/`: Contains all source code used for the analysis.
- `data/`: Instructions on how to access the blockchain data (actual data not included due to size and privacy concerns).
- `docs/`: Additional documentation and images.
- `README.md`: This file, providing an overview of the project and setup instructions.

## Tasks and Solutions
### Task 2.1: Load CSV Files
- **Objective**: Load `blocks.csv` and `transactions.csv` using PySpark.
- **Solution**: Utilized PySpark's `read.csv` method with headers and inferred schema.
<img width="361" alt="image" src="https://github.com/user-attachments/assets/0e279144-9079-4130-8b25-ed92d3488ac1" />

### Task 2.2: Evaluate Top 10 Miners
- **Objective**: Determine the top 10 miners by the total size of blocks mined.
- **Solution**: Performed aggregation and sorting in PySpark to identify the top miners.
<img width="462" alt="image" src="https://github.com/user-attachments/assets/021e8cd2-55b3-4857-9e04-07c2f91ebab8" />

### Task 2.3: Convert UNIX Timestamps
- **Objective**: Convert UNIX timestamps in `blocks.csv` to readable date format.
- **Solution**: Used PySpark functions `from_unixtime` and `to_date` to format timestamps.
<img width="180" alt="image" src="https://github.com/user-attachments/assets/6a1a0ef1-7893-4016-bb6e-eb89fa249510" />

### Task 2.4: Inner Join Datasets
- **Objective**: Join `transactions.csv` and `blocks.csv` by hash fields.
- **Solution**: Handled field name ambiguities by specifying dataset origins in the join operation.
<img width="224" alt="image" src="https://github.com/user-attachments/assets/e87d5229-2f86-4e33-bf44-456689f3411b" />

### Task 2.5: Analyze September 2015 Data
- **Objective**: Analyze block production and unique senders for September 2015.
- **Solution**: Filtered and aggregated data to produce histograms of daily activities.
<img width="307" alt="image" src="https://github.com/user-attachments/assets/0e66fafd-7c81-42a5-bb43-f21e2b869585" />
  <img width="307" alt="image" src="https://github.com/user-attachments/assets/cc5d632a-3241-4c68-854c-046c94eca49f">



### Task 2.6: Analyze October 2015 Data
- **Objective**: Calculate total transaction fees for October 2015.
- **Solution**: Used gas and gas_price fields to compute fees and visualized results with histograms.
<img width="346" alt="image" src="https://github.com/user-attachments/assets/eaf56519-4a55-475e-b2f3-08964c627863" />
<img width="353" alt="image" src="https://github.com/user-attachments/assets/b14713c3-4c15-4009-ba4f-3a016c6926d0" />
<img width="353" alt="image" src="https://github.com/user-attachments/assets/14bbaa68-ab5a-4b69-a7d0-8e04c51129e8" />



## Tools and Technologies
- **Apache Spark**: Main platform for data processing.
- **Python**: Used for scripting and additional data manipulation.
- **Matplotlib**: For creating visualizations of the analysis results.

## Setup and Installation
1. **Clone the Repository**:

