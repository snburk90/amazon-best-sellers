# 📈 Amazon Product Opportunity Scoring

This project analyzes Amazon Best Seller product data to identify high-potential items for selling — based on a custom **Opportunity Score** that balances demand, value, and market competition.

## 📊 Project Overview

Using data from the Databricks Marketplace (`bright_data_amazon_best_seller_products_reviews_products_dataset.datasets.amazon_best_seller_products`), we explore product-level insights across:

- Ratings
- Review volume
- Price
- Number of sellers
- Brand and category trends

We calculate a custom **Opportunity Score** to rank products that are:
- Highly rated
- Well-reviewed
- Competitively priced
- Underrepresented by other sellers

## 🧠 Opportunity Score Formula

```python
opportunity_score = (RATING × log(REVIEWS_COUNT + 1)) / (FINAL_PRICE × log(NUMBER_OF_SELLERS + 1))
