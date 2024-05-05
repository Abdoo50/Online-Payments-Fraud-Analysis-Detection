# Online Payments Fraud Analysis & Detection

## Project Overview

This notebook presents a thorough analysis and detection of fraud in online payment transactions. It aims to utilize advanced data processing techniques and machine learning to identify fraudulent activities, leveraging a rich dataset of financial transactions.

## Dataset Description

The dataset comprises detailed records of online payment transactions over a period of 30 days, simulating typical activities within financial services, particularly focusing on emerging mobile money transactions domains. Key features include:

- **step**: Maps a unit of time in the real world; 1 step is 1 hour of time. Total steps: 744 (30 days simulation).
- **type**: Types of transactions (CASH-IN, CASH-OUT, DEBIT, PAYMENT, TRANSFER).
- **amount**: Amount of the transaction in local currency.
- **nameOrig**: Customer who started the transaction.
- **oldbalanceOrg**: Initial balance before the transaction.
- **newbalanceOrig**: New balance after the transaction.
- **nameDest**: Customer who is the recipient of the transaction.
- **oldbalanceDest**: Initial balance of the recipient before the transaction.
- **newbalanceDest**: New balance of the recipient after the transaction.
- **isFraud**: Transactions made by fraudulent agents within the simulation.
- **isFlaggedFraud**: Flags large illegal transfers.

## Data Preprocessing

- **Renaming columns** for clarity.
- **Handling outliers** and **data quality issues** using statistical methods.
- **Feature engineering** to enhance model performance.
- **Data standardization** and resampling to address imbalanced classes.

## Data Analysis and Insights

- **Transactional Analysis**: Analyzing total transaction amounts by type, identifying high-frequency accounts, and observing post-transaction balance changes.
- **Fraud Analysis**: Focused on relationships between transaction amounts and fraudulent activities, including flagged transactions.
- **Temporal Patterns**: Examining the timing of transactions to detect any patterns related to fraud occurrences.
- **Distribution Analysis**: Comparing the distribution of amounts in fraudulent versus non-fraudulent transactions.

## Feature Engineering

- **Categorical Encoding**: Transformation of categorical transaction types using `LabelEncoder`.
- **Dropping irrelevant features**: Such as `SenderAccountId` and `RecipientAccountId`.

## Model Development and Evaluation

- **Random Forest Classifier** used with hyperparameter tuning via `GridSearchCV`.
- **Model Performance**: Evaluated using accuracy, with details on the best parameters found and test accuracy results.

## How to Use

1. **Clone the GitHub repository**:
   ```bash
   git clone [repository-url]
   ```
2. **Navigate to the notebook directory**:
   ```bash
   cd [repository-directory]
   ```
3. **Run the Jupyter Notebook**:
   ```bash
   jupyter notebook [notebook-name].ipynb
   ```

## Requirements

- Python 3.x
- Jupyter Notebook
- Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn

## Contributing

Contributions to this project are welcome. Please fork the repository, make your changes, and submit a pull request.

## License

This project is released under the MIT License. See the LICENSE file in the repository for more details.

## Contact

If you have any questions or would like to discuss this project further, please contact the repository owner or submit an issue in the GitHub repository.
