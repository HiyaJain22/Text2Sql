Overview
The Text2SQL Converter is an AI-powered tool designed to bridge the gap between non-technical users and databases. This project leverages state-of-the-art natural language processing (NLP) models to translate plain-text questions into SQL commands, making database interactions accessible for everyone.

Features
Converts natural language queries into SQL commands.
Utilizes the BART Transformer model fine-tuned for text-to-SQL tasks.
Built upon robust datasets like WikiSQL and Spider, comprising over 78,000 query pairs.
Employs SQLGlot for SQL query parsing and optimization.
Evaluated using BLEU scores for accurate performance measurement.
Repository Link
Explore the repository here.

Data Source and Preparation
The project utilizes the WikiSQL and Spider datasets, which include thousands of natural language queries paired with their SQL equivalents.

Data Processing Steps:
Data loaded and preprocessed using Python.
Integrated with SQLGlot for query optimization and column type inference.
Final dataset used for training and testing the BART model.
How to Use
Follow these steps to set up and run the project:

Clone the repository:

bash
Copy code
git clone https://github.com/HiyaJain22/Text2Sql.git
cd Text2Sql
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Run the text-to-SQL script:

bash
Copy code
python run_text2sql.py
Input a natural language query and receive the generated SQL command.

Example:
python
Copy code
from text2sql import generate_sql

query = "List all customers who placed an order in 2022."
sql = generate_sql(query)
print(sql)  # Output: SELECT * FROM customers WHERE order_date BETWEEN '2022-01-01' AND '2022-12-31';
Model and Architecture
Model:
BART (Bidirectional and Auto-Regressive Transformers):
Combines a bidirectional encoder and autoregressive decoder.
Trained with corruption techniques to enhance natural language understanding and reconstruction.
Architecture:
User Input: A plain-text query is provided by the user.
BART Model: Processes the input and generates an equivalent SQL command.
SQLGlot: Refines the generated SQL syntax and ensures accuracy.
Performance Evaluation
Fine-tuned model hosted on Hugging Face: Text2SQL BART Model.
Evaluation metrics: BLEU scores are used to validate translation quality.
Prerequisites
Python: Version 3.8 or higher.
Required libraries: transformers, SQLGlot, pandas, numpy, scikit-learn.
Screenshots
Input and Output Example:


Model Architecture Visualization:


Contributing
Contributions are welcome! If you want to contribute to this project:

Fork the repository.
Create a feature branch:
bash
Copy code
git checkout -b feature-name
Commit your changes:
bash
Copy code
git commit -m "Added feature X"
Push to the branch:
bash
Copy code
git push origin feature-name
Open a pull request for review.
Contact
For questions or suggestions, please reach out to us:

Hiya Jain: hiyajain22@example.com
Aryann Tated: aryann.tated@example.com
Yash Thakar: yash.thakar@example.com
