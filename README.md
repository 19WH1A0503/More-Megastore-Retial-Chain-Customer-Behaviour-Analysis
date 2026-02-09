# More-Megastore-Retial-Chain-Customer-Behaviour-Analysis

# Overview
More Megastore is a mojor Indian food and grocery chain operating hunderederds of supermarkkets across major cities. The company has significant amount of data on customer demographoics, shopping behaviour, engagement.
This project analyzes customer shopping behavior for a retail business to identify purchasing patterns, customer segments, and product performance drivers. The objective was to convert raw transactional and behavioral data into insights that support decisions across marketing, pricing, subscriptions, and delivery strategy.
The work follows a company-style analytics workflow, moving from data preparation to database analysis and stakeholder-ready reporting.

# Business Objective
Leadership observed shifts in customer purchasing patterns across demographics, product categories, promotions, and sales channels.
The goal was to answer:
Which customer segments drive the most revenue?
How do discounts and subscriptions influence spending behavior?
Which products perform well organically vs relying on promotions?
Where should the business focus retention and delivery investments?

# Data Overview
The dataset represents one record per customer, capturing their most recent purchase along with historical behavior indicators.
Key attributes include:
Demographics: age, gender
Product details: item, category, size, color, season
Transaction metrics: purchase amount, discounts
Engagement signals: review rating, subscription status
Behavioral indicators: previous purchases, purchase frequency
Fulfillment details: shipping type, payment method
Known limitations
No full transaction history per customer
Prior activity represented as aggregate indicators
Realistic constraint reflecting typical corporate data access



# Analytical Approach
<ul>
<li> Data Preparation (Python)
Loaded and inspected raw customer data
Identified and addressed missing values using category-level median imputation for review ratings
Standardized column naming for cross-platform consistency
Engineered new analytical features:
Age-based customer groups
Numeric purchase frequency (days between purchases)
Removed redundant promotional fields after validation
  </li>
  <li>
Database Analysis (PostgreSQL)
Persisted cleaned data into a relational database
Used SQL for business-driven analysis, including:
Revenue breakdowns by demographic segments
Discount dependency by product
Customer segmentation using behavioral thresholds
Product rankings using window functions
Subscription adoption among repeat buyers
SQL queries are organized by analytical theme for readability and reuse.
</li>
  <li>
    <img width="1007" height="551" alt="Screenshot 2026-02-08 at 8 06 55 pm" src="https://github.com/user-attachments/assets/dadff666-fc5b-4654-a73b-2beb262da8cb" />
Visualization & Reporting (Power BI)
Built an interactive dashboard for stakeholder consumption
Created KPI cards for customer count, average spend, and ratings
Designed slicers for dynamic filtering by:
Subscription status
Gender
Product category
Shipping type
Focused visuals on revenue drivers and customer segments rather than decorative charts
    </li>
</ul>

# Key Insights
<ul>
<li>Younger customer segments contributed the highest share of revenue</li>
  <img width="362" height="121" alt="Screenshot 2026-02-08 at 8 03 57 pm" src="https://github.com/user-attachments/assets/1a8f0a8b-5ac7-4a32-aa2b-a6ee6d42cb0e" />
<li>Customers using express shipping showed higher average purchase amounts</li>
<li>Several products relied heavily on discounts, signaling pricing sensitivity</li>
<li>A large portion of repeat buyers were not enrolled in subscriptions</li>
<li>High-rated products presented opportunities for premium positioning</li>
</ul>

# Business Recommendations
<ul>
<li>Expand express shipping options to high-value customer segments</li>
<li>Reassess discount strategies for products with strong organic demand</li>
<li>Target repeat buyers with subscription-focused campaigns</li>
<li>Align marketing efforts with age groups driving the majority of revenue</li>
<li>Prioritize inventory and promotion for top-performing product-category pairs</li>
</ul>
