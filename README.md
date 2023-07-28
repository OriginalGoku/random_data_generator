**Introduction**
Welcome to the Synthetic Financial Data Generation repository. This codebase uses Python and Pandas to generate synthetic data for various financial assets including equities, forex, futures, and CFDs.

In finance, backtesting, anomaly detection, and strategy evaluation require a considerable amount of historical data, which is sometimes not available or too expensive to access. This project aims to mitigate this problem by providing a method to generate synthetic but realistic financial data.

The method applied in this codebase considers the relative changes of open, high, low, and close prices of each asset by logarithmically comparing them with previous price points. The first row is discarded due to NaN values that appear as a result of this computation. The data is then shuffled to provide randomness and simulate the volatile nature of financial markets. Using this shuffled data and an initial open price, the algorithm generates synthetic data that mirrors the market's relative changes in prices.

**Synthetic Data Structure**
The generated synthetic data is structured as a list of dictionaries, where each dictionary represents a row in the DataFrame. Each row is calculated based on the close price of the previous row and relative prices of the current row. This list is then converted back to a DataFrame for easier manipulation and analysis.

**Usage**
To use this code, replace the 'spy.csv' in the line df = pd.read_csv('spy.csv', index_col=[0], parse_dates=True) with the path to your input file. The input file should be a CSV file with columns for open, high, low, and close prices.

**Licensing**
This codebase is distributed under the terms of the Apache License 2.0. The full terms and conditions of this license are detailed in the LICENSE file.

**Disclaimer**
While this codebase is designed to generate synthetic financial data, it's important to note that no synthetic data can perfectly mirror the intricacies and unpredictable nature of real-world financial markets. This codebase should be used as a tool to supplement financial analysis and testing, not as a standalone decision-making tool.

**Contributions**
Contributions to this codebase are always welcome. Whether it is improving the algorithm, adding additional features or fixing bugs, feel free to make a pull request or raise an issue.

Remember, while this repository provides a useful tool for financial data generation, it should be used responsibly, considering all the risk factors associated with financial decision-making. Enjoy your exploration!

Happy Coding!
