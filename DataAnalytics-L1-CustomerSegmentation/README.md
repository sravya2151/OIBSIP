\# Customer Segmentation Analysis



\## Project Overview



This project performs customer segmentation for an e-commerce business using RFM (Recency, Frequency, and Monetary) analysis and K-Means clustering.



The objective is to identify distinct customer groups based on purchasing behaviour and provide targeted marketing recommendations for each segment.



\## Dataset



The project uses the Online Retail dataset containing transactional data from an e-commerce business.



The dataset includes information such as:



\* Invoice number

\* Product code

\* Product description

\* Quantity

\* Invoice date

\* Unit price

\* Customer ID

\* Country



\## Technologies Used



\* Python

\* Pandas

\* NumPy

\* Matplotlib

\* Seaborn

\* Scikit-learn

\* Jupyter Notebook

\* OpenPyXL



\## Data Cleaning



The following preprocessing steps were performed:



\* Removed cancelled transactions

\* Removed records with missing Customer IDs

\* Removed duplicate records

\* Removed transactions with non-positive quantities

\* Removed transactions with non-positive unit prices

\* Created a `TotalAmount` feature using Quantity × UnitPrice



After cleaning, the dataset contained 392,692 transaction records.



\## RFM Analysis



Customer behaviour was analysed using three key features:



\* \*\*Recency:\*\* Number of days since the customer's most recent purchase

\* \*\*Frequency:\*\* Number of unique invoices/orders made by the customer

\* \*\*Monetary:\*\* Total amount spent by the customer



Additional metrics calculated were Average Purchase Value and Customer Lifetime Value proxy.



\## Customer Segmentation



The RFM features were standardized using `StandardScaler`.



The Elbow Method was used to determine a suitable number of clusters. Based on the analysis, \*\*4 clusters\*\* were selected.



K-Means clustering was then applied to segment the customers.



\### Customer Segments



| Cluster | Segment                      |

| ------- | ---------------------------- |

| 0       | Regular Customers            |

| 1       | At-Risk / Inactive Customers |

| 2       | Champions / VIP Customers    |

| 3       | Loyal High-Value Customers   |



\## Marketing Recommendations



\### Regular Customers



Use personalized product recommendations, product bundles, and loyalty rewards to encourage repeat purchases.



\### At-Risk / Inactive Customers



Use win-back emails, special discounts, and limited-time offers to encourage customers to return.



\### Champions / VIP Customers



Provide VIP rewards, exclusive products, early access, and premium customer service.



\### Loyal High-Value Customers



Encourage repeat purchases through loyalty programs, cross-selling, and personalized offers.



\## Visualizations



The project includes:



\* Elbow Method plot

\* Number of Customers per Cluster

\* Recency vs Monetary scatter plot

\* Frequency vs Monetary scatter plot



The visualizations are available in the `images` folder.



\## Conclusion



Customer segmentation helps an e-commerce business understand purchasing behaviour and identify groups with different levels of engagement and value. The results can be used to develop targeted marketing strategies, improve customer retention, and focus resources on high-value customers.



\## Project Structure



```text

DataAnalytics-L1-CustomerSegmentation/

│

├── Customer\_Segmentation\_Analysis.ipynb

├── Online Retail.xlsx

├── README.md

├── requirements.txt

└── images/

&#x20;   ├── elbow\_method.png

&#x20;   ├── customers\_per\_cluster.png

&#x20;   ├── recency\_vs\_monetary.png

&#x20;   └── frequency\_vs\_monetary.png

```



